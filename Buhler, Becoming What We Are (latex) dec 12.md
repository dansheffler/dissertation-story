%!TEX TS-program = xelatex
%!TEX encoding = UTF-8 Unicode

\documentclass[11pt,letterpaper,oneside,titlepage,openright]{book}
\usepackage[utf8]
{inputenc}
\usepackage{epigraph}


% Use fonts from system fonts.
\usepackage{fontspec,xunicode}
\defaultfontfeatures{Mapping=tex-text}
\setmainfont[Mapping=tex-text]{Baskerville}
{\catcode`\ =\active{\global\let =\ }}
\everymath{\catcode`\ =\active}

\newcommand{\textsubscr}[1]{\textsubscript{#1}}

\usepackage[leftmargin=0.5in,rightmargin=0.5in,noorphans,indentfirst=false]{quoting}

\makeatletter
\newcommand*{\@doendeq}{%
  \everypar{{\setbox\z@\lastbox}\everypar{}}%
}

\renewenvironment{quote}{%
    \singlespacing\begin{quoting}%
}{%
    \end{quoting}\ignorespacesafterend\par\noindent\aftergroup\@doendeq%
}
 
\makeatother

\let\origfootnotesize\footnotesize
\let\footnotesize\normalsize

\usepackage[notes,isbn=false,url=false,citereset=chapter]{biblatex-chicago}
\addbibresource{mybib.bib}

\usepackage{footmisc}
\makeatletter
\renewcommand\@makefntext[1]{% 
    \parindent 0.5in% 
    \@thefnmark.~#1}
\makeatother

\usepackage[xetex, bookmarks, colorlinks=false, pdftitle={}, pdfauthor={}, pdfsubject={}]{hyperref}


\usepackage[shortlabels]{enumitem}
\setlistdepth{35}



\usepackage{afterpage}


%%%%%%%%%%%%%%%%%% Pandoc's Presets %%%%%%%%%%%%%%%%%%%%%%%%%%%

\IfFileExists{upquote.sty}{\usepackage{upquote}}{}
\IfFileExists{microtype.sty}{%
\usepackage{microtype}
\UseMicrotypeSet[protrusion]{basicmath} % disable protrusion for tt fonts
}{}

\date{}


\usepackage[right=1in,left=1.5in,top=1in,bottom=1in,includehead]{geometry}
\usepackage{setspace}
\parindent  0.5in

% List Environments
\setlist[enumerate]{%
    labelindent=0.5in,%
    leftmargin=*,%
     nosep%
}
\setlist[itemize]{%
    leftmargin=0.5in,%
    labelindent=0.0in,%
    labelsep=*%
}

\makeatletter
\let\oldenumerate=\enumerate
\renewenvironment{enumerate}{%
    \singlespacing\begin{oldenumerate}
}{%

\end{oldenumerate}\ignorespacesafterend\par\noindent\aftergroup\@doendeq}
\makeatother

\usepackage[bottomtitles,explicit]{titlesec}

\titleformat{\chapter}[display]{\vspace{1in}\bfseries\normalsize}{Chapter \thechapter \normalsize\newline #1}{0.2in}{}[\vspace{-1in}]

\titleformat{\section}[hang]{\bfseries\normalsize}{\arabic{section}. ~~#1}{0in}{}

\titleformat{\subsection}[hang]{\bfseries\normalsize}{\arabic{section}.\arabic{subsection} ~~#1}{0in}{}

\titleformat{\paragraph}[hang]{\bfseries\normalsize}{\Roman{section}.~~#1}{0in}{}

\titleformat{name=\subsection,numberless}[hang]{\bfseries\normalsize}{#1}{0in}{}






\titleformat{\subsubsection}[runin]{\normalsize}{}{0.5in}{\hspace{0.5in}}
\titlespacing*{\subsubsection}{0.5in}{0in}{0in}

\titleformat{\subsubparagraph}[runin]{}{}{.5in}{}

% Reset subsubsection counters even if levels are skipped.
\makeatletter
    \@addtoreset{subsubsection}{section}
\makeatother



% Page Header Formating
\usepackage{fancyhdr}
\setlength{\headheight}{15.2pt}
\usepackage{lastpage}

\pagestyle{fancy}


\fancypagestyle{plain}{%
\fancyhf{} % clear all header and footer fields
\fancyfoot[C]{\thepage} % except the center
\renewcommand{\headrulewidth}{0pt}%
\renewcommand{\footrulewidth}{0pt}%
\newgeometry{top=1in,left=1.5in,right=1in,bottom=1in}
}

\fancypagestyle{none}{%
\fancyhf{} % clear all header and footer fields
\renewcommand{\headrulewidth}{0pt}%
\renewcommand{\footrulewidth}{0pt}%
\newgeometry{top=1in,left=1.5in,right=1in,bottom=1in}
}


% Header that’s working just fine 
\fancypagestyle{myheading}
{\lhead{\rightmark}\chead{}\rhead{}}


\fancyfoot[C]{\thepage} 
\renewcommand{\headrulewidth}{1pt}%
\renewcommand{\footrulewidth}{0pt}%


\clubpenalty=1000
\widowpenalty=1000


%%


\begin{document}

% Fixes for sections in the header.
\pagestyle{myheading}
\renewcommand{\chaptermark}[1]{\markright{\chaptername\ \thechapter: \ #1}}
\renewcommand{\sectionmark}[1]{\markright{\chaptername\ \thechapter, Section \arabic{section}: \ #1}}



    % Exclude header from first page
    \thispagestyle{plain}


    % % Title
    % \vspace{.1in}


    % The rest of the paper

\doublespace


%%%%%%% Pandoc Presets %%%%%%%

\frontmatter
\thispagestyle{empty} \par\vspace*{.1\textheight}
\begin{center}



BECOMING WHAT WE ARE:    

VIRTUE AND PRACTICAL WISDOM AS NATURAL ENDS




\par\vspace*{.1\textheight}
\line(2,0){200}


DISSERTATION  

\line(2,0){200}
\par\vspace*{.1\textheight}






A dissertation submitted in partial fulfillment    

of the requirements for the degree of Doctor of Philosophy 

in the  College of Arts and Sciences       

at the University of Kentucky     

By 
    
Keith Buhler

Director: Dr. David Bradshaw, Professor of Philosophy

Lexington Kentucky

Copyright © Keith Buhler 2016  




\end{center}
\newpage
\thispagestyle{empty}

\begin{center}

ABSTRACT OF DISSERTATION 


\end{center}
\begin{singlespace}

This dissertation is about ethical naturalism. Philippa Foot and John McDowell both defend contemporary neo-Aristotelian ethics but each represents a rival expression of the same. They are united in the affirmation that virtue is ‘natural goodness’ for human beings; they are divided in their rival conceptions of ‘nature.’ McDowell distinguishes second nature or the "space of reasons" from first nature or the “realm of law.” Foot rejects this division.


On Foot's naturalism, natural goodness is a just as much a feature of first nature as health is, even though human practical reasoning is unique in the biological world. I defend Foot’s view by appealing to “generic propositions,” a little-utilized feature of linguistic theory. Life forms and functions described in generic statements are intrinsically normative and yet just as scientifically respectable as other naturalistic concepts. Hence, the generic proposition that "humans are practical, rational primates" has both descriptive and normative content. It follows that the ethical and rational norms defining a good human life are a subset of natural norms which can be known as such from an “external” scientific point of view as well as from an “internal” ethical point of view. 

Going beyond Foot’s views, I present a new interlocking neo-Aristotelian account of virtue and practical reason. Virtues are excellences of practical reasoning and rational practice. Virtues enable and partly constitute a good life for human beings. Practical reasoning is the ability to pursue perceived goods and avoid perceived evils in every action. Practical wisdom, which is excellence in practical reasoning, is the master virtue that enables one to succeed in becoming truly human, despite varying abilities and life circumstances. In short, all of us ought to pursue virtue and practical wisdom because of what we are; virtue and practical wisdom are natural ends. 

I aim to secure the naturalistic credentials of my view by examining three influential conceptions of ‘nature,’ criticizing McDowell's conception and showing how my view is consistent with the remaining two. The resulting view is called 'recursive naturalism' because nature recurs within nature when natural beings reason about nature, about themselves, and about their own reasoning. \newline

KEYWORDS: ethical naturalism, neo-Aristotelianism, virtue, practical wisdom, natural law, natural ends

\end{singlespace}
\begin{flushright}

\underline{\hspace{.5in}Keith Buhler\hspace{.5in}}

\underline{\hspace{.3in}December 4, 2016 \hspace{.3in}}


\end{flushright}
\newpage
\thispagestyle{empty}

\hfill \break
\hfill \break
\hfill \break

\begin{center}

BECOMING WHAT WE ARE: 

VIRTUE AND PRACTICAL WISDOM AS NATURAL ENDS



\par\vspace{.05\textheight}

By

Keith Buhler

\end{center}
\begin{singlespace}

\par\vspace{.2\textheight}

\begin{flushright}

\underline{{\hspace{.4in}} Dr. David Bradshaw \hspace{.4in}}

Dissertation Director

\hfill \break

\underline{{\hspace{.5in}} Dr. Clare Batty {\hspace{.6in}}}

Director of Graduate Studies 


\hfill \break

\underline{{\hspace{.6in}}December 4, 2016{\hspace{.4in}}}


\end{flushright}

\end{singlespace}
\newpage
\thispagestyle{empty} \par\vspace*{.10\textheight}
\begin{center}



For Lindsay Elizabeth. 

\begin{em}"Oh, who shall understand but you; yea, who shall understand?"\end{em}






\end{center}
Acknowledgments
===============

\thispagestyle{empty}

\begin{center}

ACKNOWLEDGMENTS

\end{center}
\begin{singlespace}

I am sincerely grateful to Dr. David Bradshaw for being my advisor on this project. He was not only a professor but a model of virtue and practical wisdom. I am also grateful for the early encouragement of friends and family members such as Kristi Buhler, who first taught me to dream big, and John Mark Reynolds, who first told me I was a philosopher. Alfred Geier, whom students have characterized as "Zeus in human form," mentored me in philosophical dialogue, while Gary Hartenburg's invaluable feedback helped me transition into graduate school. Timothy Sundell first pushed me toward serious research in metaethics, and Anita Superson helped with early and tough criticism of my project. I am especially grateful to Stefan Bird-Pollan and Dan Breazeale  for saving the day and serving on my committee last minute. Once I began writing in earnest, Lindsay Buhler was the first to read and edit each chapter. Even before a chapter was written, she played the role of Socratic midwife, testing each new idea to see if it was viable or only a "wind egg." Michael Garten was the last to read and edit each chapter, providing incisive objections I can only hope I have adequately overcome. Great strides in the construction of this dissertation would have been impossible without the very practical help of a few others: Dan Sheffler trained me, like his father trained him, in the ways of formatting in Markdown and LaTeX. Also, the University of Kentucky Graduate School hosted a writing boot camp to help folks like me to write intensively for two weeks. Eric Peterson was not only a fellow companion in graduate school but a friend and source of encouragement. Finally, the United Way of the Blue Grass generously donated tuition dollars, books, and the laptop computer on which I wrote this dissertation.  These people, and more whom I forgot to name, helped bring this project to fruition. My late father, Dr. Rich Buhler, received two honorary doctorates for his work in radio. I recently found out that he told others (when I had just started college) that he suspected I would be his first child to receive an earned doctorate. I was happy to learn this; I am even happier now to justify his suspicion. 



\newpage
\thispagestyle{empty}



\tableofcontents

\end{singlespace}
\newpage
\thispagestyle{empty} \par\vspace*{.3\textheight}
\setlength{\epigraphwidth}{.98\textwidth}
\begin{epigraphs}
\qitem{γένοι' οἷος ἐσσὶ μαθών. (Become what you are, having learned what that is.)}%
{---\textsc{Pindar, \begin{em} Pythian \end{em} 2, line 72.}}
\centering
\end{epigraphs}
\mainmatter

Many Sorts of Naturalism
========================

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{The most striking occurrence in the history of thought between Aristotle and ourselves is the rise of modern science.}%
{---\textsc{John McDowell, \lq\lq Two Sorts of Naturalism,\rq\rq 174.}}
\centering
\end{epigraphs}
Nature and Ethics
-----------------

This dissertation is about ethical naturalism. But what is ‘naturalism’?
There is no consensus as to the meaning of the term. Should we then
simply stipulate a meaning and move on? I do not think we should. Almost
a century ago, Roy Wood Sellars said it well: “Questions of terminology
are less superficial than is often supposed. Precision in terminology
usually accompanies clear thinking, and is at once its condition and
effect.”[@sellars1927naturalism .] Sellars is one of many other
philosophers over the last hundred years to have taken pains to clarify
the difference between his view – naturalism – and materialism. Why? Is
there any point in labeling any view, much less an ethical view, as
“naturalistic”?

The answer, in part, is that the term ‘nature’ and its cognates
‘naturalism’ and ‘naturalistic’ are philosophically potent; they are
what Richard Weaver calls “god terms.” God terms are words and phrases
that, though vague, have an indelible, inherently positive,
connotation.[@weaver1985ethics] If this is right, then Sellars (and
others) are so concerned to establish the naturalistic credentials of
their view for two reasons: first, whatever philosophical theories earn
the right to the label acquire an automatic positive connotation; and
secondly, the potency of ‘nature’ derives, in part, from its connection
to another god term – namely, science. ‘Science’ and ‘nature’ are often
simply defined *in terms of each other*. To pull a few examples out of
dozens: “nature is, more or less, what our latest and best science tells
us it is;”[@brown2008virtue 2] “moral facts exist only if they can
figure in our best scientific explanations;”[@cuneo2007 50] “Natural
facts are understood to be facts about the natural world, facts of the
sort in which the natural sciences trade.”[@sepmoralnaturalism,
introduction.] In short, the sciences study nature and nature is
whatever the sciences study. This way of talking is very inadequate and
very common. (I shall try state things more adequately in chapter 6.)

What, then, is ethical naturalism? Even before clarifying our terms, we
can understand it as the venturesome pursuit a “scientific ethics” or
“ethical science.” If successful, ethical naturalists can attach to
their moral theory part of the aura of objectivity we attach to science.

My project in what follows is to work toward a theory of virtue and
practical reason that is consonant with, and reinforced by, a plausible
version of scientific naturalism. To many, such a project seems
depressingly ill-fated. On the one hand, a genuinely *normative* virtue
theory that is consistent with scientific naturalism might seem
impossible. For example, Stephen R. Brown’s recent defense of
neo-Aristotelian ethical naturalism argues that “an individual human
being may be evaluated as good or bad according to how well that
individual realizes the human way of life” but even he concedes that his
account is “in the end… fundamentally descriptive.”[@brown2008virtue 1]
Arthur Ward, likewise, thinks that the “traditional objections to virtue
ethics” are decisive. He argues that “facts about human nature do not on
their own seem to generate reasons for humans to act in accordance with
their nature.”[@ward2013against 35]

On the other hand, ethical naturalism might seem undesirable. For
example, it runs afoul of the widely-assumed division between science
and ethics. On this assumption, theoretical disciplines such as physics
and biology study objects, their properties and so on, while practical
disciplines study values and social norms, etc. The natural sciences
study factual and descriptive matters, while the disciplines that used
to be called the “moral sciences”[^1] study evaluative and normative
matters. On this assumption, each kind of discipline is autonomous. And
most thinkers are content to leave it that way.

One of the many pitfalls into which a putative “scientific ethics” might
fall is a scientific encroachment on ethics. For example, E.O. Wilson
boldly stated that “the time has come for ethics to be removed
temporarily from the hands of the philosophers and biologicized.”[^2]
Thankfully, scientific thinkers are not usually so zealous to abduct a
philosophical discipline (nor are philosophers, as a rule, eager to
surrender them) but there is a legitimate danger of appearing to license
such encroachment.

An equal and opposite pitfall would be that ethics might encroach on
science. While working scientists must certainly adhere to legal,
professional, and rational norms in conducting and presenting their
research, it seems a bit much to suggest that they should be accountable
to moral philosophers. In light of these pitfalls professional and
philosophical pitfalls, perhaps the widespread assumption that science
and ethics are autonomous is the safer course.

There are two main ethical alternatives to naturalism that follow the
safer course of accepting the fundamental divide between science and
ethics. The first alternative is ethical *non-naturalism*, classically
articulated by G. E. Moore and (more recently) by Russ
Shafer-Landau.[@moore; @shafer2003moralrealism] Non-naturalist views
argue that (even if moral facts are *realized* by natural facts) moral
facts are neither identical to natural facts nor fully reducible to
natural facts. Accordingly, philosophers such as Moore and Shafer-Landau
conclude that moral philosophy proceeds independently of the methods of
“natural philosophy” (i.e., the natural sciences). Non-naturalism allows
one to embrace “robust realism” about morality and practical
reasoning.[^3]

The second alternative – equally safe for scientific naturalists – is to
reject robust realism. This alternative encompasses a variety of quite
different views, such as as error theory, expressivism, subjectivism,
moral nihilism, and perhaps others. The underlying motivation for
denying robust realism is the perceived incompatibility of robust
ethical realism with the modern scientific worldview. This is evident in
anti-realism’s main defenders. For example, John Mackie admits that “the
main tradition of European moral philosophy” accepts objective values
but argues that modern science has overthrown all that. Likewise, Simon
Blackburn commends anti-realism because it asks “no more of the world
than we already know is there – the ordinary features of things on the
basis of which we make decisions about them, like or dislike them, fear
them and avoid them, desire them and seek them out. It asks no more than
this: a natural world, and patterns of reaction to
it.”[@blackburn1985spreading] And Jay Wallace explains that expressivism
offers a “naturalistic interpretation of practical reason… that may seem
appropriate to the enlightened commitments of the modern scientific
world view… it makes no commitment to the objective existence in the
world of such allegedly questionable entities as values, norms, or
reasons for action.”[@seppracticalreason]

Neo-Aristotelian Ethical Naturalism
-----------------------------------

In spite of these formidable difficulties, this dissertation commends
the riskier course of pursuing ethical naturalism – specifically,
neo-Aristotelianism. Contemporary neo-Aristotelians – among others[Cf.
@harmon] – have offered a serious challenge to the assumed divide
between norms and nature or facts and values. Accordingly, they have
challenged the comfortable assumption that science and ethics can be
neatly divided. Perhaps it is possible to offer an account of human
biology and society that is both scientifically robust *and* normatively
significant. Perhaps there are moral facts about what human beings are
and ought to be that we can discover by engaging in practical reasoning.
Perhaps success as moral agents depends on how well we conform our lives
to the ways human beings ought to live.

There are, of course, other forms of ethical naturalism, such as Cornell
Realism and Frank Jackson’s functionalism.[^4] They share with
neo-Aristotelian the insistence that some moral facts *are* identical to
– or reducible to – natural facts – and hence that moral philosophy
*can* and *should* employ methods similar to those employed in the
natural sciences. But what is remarkable is that neo-Aristotelian theory
has avoided some of the pitfalls mentioned above. Rather than licensing
unjust encroachment of some disciplines over others, it has become a
thriving research program across disciplines. Neo-Aristotelianism is
making inroads in moral philosophy, metaphysics, philosophy of science,
as well as in the medical, social, and political sciences.

On the neo-Aristotelian account, the premises about human nature as
practical reasoners are intrinsically related to normative conclusions
about what one ought to do. As Rosalind Hursthouse explains, evaluations
of plants, animals, and humans all “depend upon our identifying what is
characteristic of the species in question.”[@hursthouse1998virtue
chapter 10, abstract.] In other words, the *normative evaluation*
depends on the *descriptive facts* of the species: its activities, its
life form, and so on. Evaluating things on the basis of what they are is
central to neo-Aristotelian naturalism.

Alasdair MacIntyre articulates the intrinsic relationship between human
nature and human ethics – a particular kind of ‘is’ and ‘ought’ – with
his discussion of the three “elements” of morality.[@macintyre1984after
54 ff] The first element is “untutored human nature” (as it is).
Understanding “human-nature-as-it-is”[@macintyre1984after 55] is a task
for philosophers, as well as psychologists, sociologists,
anthropologists, etc. and would include a conception of the human
species as rational animals as it is *prior* to deep self-reflection or
moral effort. The second element is humanity as it could be and should
be – what MacIntyre calls
“man-as-he-could-be-if-he-realized-his-telos.”[@macintyre1984after 55]
Understanding the natural human ends we can and *ought* to pursue is,
for MacIntyre, “the whole point of ethics.” The third element is the set
of virtues, actions, emotions, etc., needed to move from the first to
the second points. For MacIntyre, positing a normative theory such as
virtue ethics is futile without the other two elements.

I think MacIntyre’s “three elements” also help to explain the puzzle of
why ‘neo-Aristotelianism’ is both a substantive normative theory and a
metaethical theory. Foot and McDowell not only defend ethical naturalism
but commend the pursuit of virtues such as courage, moderation, justice,
and practical wisdom, among others. Is the conflation of metaethics and
normative ethics a philosophical foul? Not at all. First, other brands
of moral realism closely align with particular normative commitments:
Frank Jackson and the Cornell Realists tend to endorse a form of
consequentialism or welfarism. Richard Boyd explains:

> Many naturalist moral realists have also advocated some version or
> other of consequentialism as the substantive naturalist moral theory
> to which they are committed. Indeed, although nothing like entailment
> between these positions obtains, the idea that moral questions are
> questions about how we can help each other flourish seems central to
> contemporary naturalist moral realism. In a certain sense, some
> version of consequentialism seems to be the natural position for
> naturalist moral realists.[@boyd2003finite 505-6]

Secondly, the question of whether metaethics and normative ethics are
even separable is a dispute that cannot be settled out of court. Allan
Gibbard narrates how the hard line distinction between substantive
ethical matters and formal metaethical matters originated in the
writings of G.E. Moore. And, at the risk of understatement, not everyone
agrees with Moore:

> Some philosophers have rejected the distinction; some Kantians, for
> instance, think that if you get the metatheory right, substantive
> ethical conclusions fall out as some kind of consequence, so that
> metaethics and substantive ethics are not really separate… Those who
> reject any systematic distinction between questions of meaning and
> questions of substance might likewise reject a sharp, separate subject
> of metaethics.[@gibbard2003normative 320]

Rosalind Hursthouse, Alasdair MacIntyre, Philippa Foot, and John
McDowell are other good examples of philosophers who think that
metaethics and substantive ethics are not ultimately separable. I follow
them in this. My thesis will commend the acquisition of character and
epistemic virtues *and* will analyze normative terms in a way consonant
with a plausible version of scientific naturalism.

I think these brief comments are sufficient to demonstrate three truths
about neo-Aristotelianism: (a) it is avowedly ambitious and equally
unsettling; (b) it faces titanic opposition on terminological and
academic grounds no less than philosophical ones; and thus, (c) it is a
significant theory in normative ethics and beyond.

The remainder of this introduction explains why I focus more on Foot’s
*Natural Goodness* rather than Hursthouse’s *On Virtue Ethics*, and
provides an initial characterization of the contrast between Foot’s and
McDowell’s rival sorts of ethical naturalism.

On Natural Goodness and Virtue Ethics
-------------------------------------

Philippa Foot’s *Natural Goodness* is one of the rare philosophical
monographs that manages to be a work of art. One reviewer warned that it
is “so gracefully written that the reader runs the risk of… mistaking
the book’s fluidity for shallowness. In fact, the depth… is
remarkable.”[@sadler2004review] Indeed, it is a delight to read for its
elegance and pugnacity, but it is a duty to read for its wisdom and
profundity. Building on her prior work in virtue theory, Foot blends
metaethics and normative ethics by laying the foundation for what Mark
Murphy calls a “secular natural law theory.”[@sepnaturallaw] She argues
that living virtuously and wisely is natural goodness for human beings
just as hunting in packs is natural goodness for wolves.

The obvious objection to such a thesis is that it inappropriately blends
facts and values, that it either “biologizes” ethics or “enchants”
science. This obvious objection (which Foot tackles head on in her
monograph) rests on the common notion that nature and science are
entirely distinct from values and ethics. This objection is a serious
one. But it is more likely to be leveled reflexively by someone who has
not wrestled with Foot’s argument. John Hacker-Wright is correct to say
that “Foot’s recent readers have made some rather serious missteps in
approaching her work.”[@hacker2009natural 321]

Receiving an initial “cool reception”[@hacker2009natural 309] is not an
infallible sign of a classic, but it is one tell-tale sign. It is plain
from the literature that too few ethicists and metaethicists have come
to grips with the precise details and wide-ranging implications of her
argument. For example, James Barham suggests that Foot’s *Natural
Goodness* and Rosalind Hursthouse’s *On Virtue Ethics* are making the
same case, but that Hursthouse’s “account is the clearer and more
detailed of the two.”[@sepmoralnaturalism . He says, “Neo-Aristotelian
naturalism is articulated at length and along mutually similar lines in
two recent monographs, Foot’s *Natural Goodness* and Hursthouse’s *On
Virtue Ethics*.”] This comparison is misleading on two fronts.

First, even though both books are successful in their aims, they have
very different aims. Hursthouse’s book is intended to render modern
virtue ethics conventional; Foot’s book is intended to disrupt a hundred
years of metaethical convention.[@foot2001natural 5: “For better or
worse—and many will say worse—I have in this book the overt aim of
setting out a view of moral judgement very different from that of most
moral philosophers writing today.”] Hursthouse offers an olive branch to
deontologists and utilitarians, trading in her formerly combative
rhetoric for mutual respect so that iron may sharpen iron. Foot (like
Anscombe and MacIntyre) calls into question much of what has passed for
modern moral philosophy, naming names and picking fights.

Secondly, the relative clarity of the two books fits their aims.
Hursthouse’s overview of virtue ethics is aimed at non-expert graduate
and undergraduate students. It therefore exhibits some of the necessary,
though unfortunate, style of textbooks: comprehensive, responsible, and
occasionally plodding. Foot’s “fresh start”[@foot2001natural 5] is aimed
at professional ethicists. It is therefore more comparable to a Platonic
dialogue or Humean treatise: Foot plays the Socratic gadfly to the
experts with “a swaggering gait and roving eye.” Her book is
“crude”[@foot2001natural 1] because it is what Waismann calls a “living
thought,” digging deep into the soil of our presuppositions. *On Virtue
Ethics* is a thoroughly respectable book, but *Natural Goodness* makes
one proud to be a philosopher.

Happily, some ethicists *have* come to grips with the significance of
Foot’s case. For example, MacIntyre’s eventual position begins to look
similar to Foot’s position, for he defends the importance of human
biology to human ethics in his most recent ethical monograph more than
he did in *After Virtue*.[@macintyre1999dependent]

By contrast, McDowell’s opposition to scientism leads him to disagree
with Foot. McDowell’s and Foot’s respective approaches to
neo-Aristotelian ethical naturalism represent rival visions of the
relation between human beings and nature and hence between ethics and
science. As I shall show, the fault line between these rival views is of
enormous philosophical and ethical significance. The fault line between
these views is the theme of this dissertation.

Organic and Social Naturalism
-----------------------------

Foot and McDowell represent rival versions of contemporary
neo-Aristotelianism. They are united on the view that some properties
(such as virtues) are instances of ‘natural goodness’ for creatures like
us but divided on how to cash out the notion of *natural goodness*. It
is worth quoting the opening passage of McDowell’s “Two Sorts of
Naturalism” to situate the convergence and divergence of their accounts:

> Philippa Foot has long urged the attractions of ethical naturalism. I
> applaud the negative part of her point, which is to reject various
> sorts of subjectivism and supernaturalist rationalism. But I doubt
> whether we can understand a positive naturalism in the right way
> without first rectifying a constriction that the concept of nature is
> liable to undergo in our thinking. Without such preliminaries, what we
> make of ethical naturalism will not be the radical and satisfying
> alternative to Mrs Foot’s targets that naturalism can be. Mrs Foot’s
> writings do not pay much attention to the concept of nature in its own
> right, and this leaves a risk that her naturalism may seem to belong
> to this less satisfying variety. I hope an attempt to explain this
> will be an appropriate token of friendship and
> admiration.[@mcdowell1998mindvalue 167]

McDowell, like Foot, is opposed to non-naturalism and in favor of *some
sort* of naturalism. But he is also opposed to a cruder form of
naturalism which he calls “bald naturalism.” What is ‘bald naturalism’?
This is McDowell’s term for metaphysical and epistemological commitments
to crass materialism and scientism. On bald naturalism, nature is the
complete spatio-temporal cosmos. Nature includes natural causal laws but
excludes “non-natural” entities such as Platonic forms, values, norms,
and reasons along with gods, ghosts, and angels that can only be known
via empirical, scientific methods. On bald naturalism, there is no room
at all for normative, ethical knowledge unless it can be acquired
through the undue application of empirical methods to ethical matters.
McDowell thinks, instead, that if our best ethical thinking cannot be
squared with a particular dogma of empiricism, so much the worse for the
dogma. Nevertheless, McDowell also rejects ethical non-naturalism,
supernaturalism, and subjectivism.

While McDowell does not quite accuse Foot’s view of slipping into bald
naturalism, he is worried that it *might* do so or at least that it
*might be misinterpreted* as doing so. What then *does* he endorse? He
would concede that the conceptual space between non-naturalism and bald
naturalism is admittedly tight. There are two main rivals jockeying for
a position within that space. As Julia Annas explains, even rejecting
non-naturalism and bald naturalism, some neo-Aristotelians emphasize the
*biological* nature of humanity (in contrast to the odd normativity of
our rationality) while others emphasize the *rational* nature of
humanity (in contrast to the mundane descriptivity of biology).[^5] Both
views are broadly Aristotelian and broadly naturalistic, but the small
difference between them has large ramifications.

I shall dub these two rival views ‘organic naturalism’ and ‘social
naturalism’ throughout these chapters.[^6] The rivalry between organic
and social naturalism is the primary theme of this dissertation, so it
will be important to provide an initial explication of each here.

Social naturalism is the view that normativity and teleology are
intrinsic to *human nature*. On this alternative, humans are naturally
practical, social, and rational creatures who undertake to achieve their
chosen ends, as individuals and in groups. Rosalind Hursthouse, the
early MacIntyre, and (possibly) Iris Murdoch are social naturalists.[^7]
For example, in his earlier work, MacIntyre announced that his account
of virtue is “happily not Aristotelian… although this account of the
virtues is teleological, it does not require any allegiance to
Aristotle’s metaphysical biology.”[@macintyre1984after 197] The
“metaphysical biology” MacIntyre refers to here is the metaphysically
realist view that formal and final causes inhere in biological species.
His ethics is teleological only insofar as *human society and
rationality* are teleological. Otherwise, he would insist that the
natural world described by the sciences is “bald” of moral facts unless
and until it is observed, judged, and evaluated by rational agents such
as ourselves.

Organic naturalism, by contrast, is the view that normativity is
intrinsic to *organic nature*. On this alternative, natural properties
such as being alive or being healthy are objectively normative, even
prior to human evaluation. Michael Thompson, James Barham, Jennifer
Frey, the later MacIntyre, and others are organic naturalists.[For a
detailed exposition of the full menu of philosophical options, see
@perlman2004teleology . And for particular defenses of natural
normativity in the philosophy of science and the philosophy of biology,
see:
@arnhart1988; @johnson2005; @huneman2006naturalising; @leunissen2010explanation
.] They argue that simply *to be alive* is to possess a natural good; to
be healthy is to possess a natural good. Accordingly, death or
extinction, sickness or injury would be natural evils. Plants, bacteria,
and humans are similar in that thriving involves performing whatever
movements are necessary for the organism to survive, develop into
species-specific maturity, and reproduce. Organic naturalism insists
that the complex biological system on earth cannot be exhaustively and
scientifically described without normative concepts and terms.

McDowell is, by my lights, a social naturalist.[^8] He argues that we
are naturally social creatures who can speak, reason, and engage in
intentional action by “second nature”[^9] or “the space of
reasons.”[^10] McDowell’s social naturalism grounds ethics in “second
nature” – human reasoning and all that comes with it. I call his view
‘social naturalism’ because he also argues that rationality is
essentially social; we learn our first language and initial inventory of
concepts and beliefs from our family, culture, and education. In this
way, McDowell aims to afford a place for norms and reasons in “nature”
while still excluding a non-natural realm of divinity or platonic forms.
The strength of social naturalism is that it captures the commonsense
insight that human beings live in societies and create their own goals.
We not only act but act *on reasons*. The cost of social naturalism, as
I shall explain throughout these chapters, is an incorrigible cultural
relativism and an undesirable nature/human dualism.\newline
\indent Foot is an organic naturalist. Rationality is unique to humans
but is not fundamentally discontinuous with “first nature.” The strength
of organic naturalism is that it offers a more unified account of
humanity’s place within nature and promises a firm ground for the
objectivity of morality. The cost of organic naturalism seems to be a
picture of nature at odds with the scientific picture. For organic
naturalism, the question is: Are “natural norms” natural objects like
other natural objects? And how do we identify them – through normal
scientific methods or not? \newline
\indent Even for a moral naturalist, there are a variety of sorts of
naturalism on offer. The proper way to understand the debate between
Foot’s organic naturalism and McDowell’s social naturalism is as a
negotiation for the conceptual rights to the label ‘ethical naturalism’
without falling into either bald naturalism or non-naturalism. In what
follows, I attempt to move this negotiation forward. I draw primarily on
overlapping themes in the writings of Foot, McDowell, Hursthouse, and
Alasdair MacIntyre and interact with other sources as needed: from
historical sources (Aristotle, Aquinas, Hume), to other ethicists
(Bernard Williams, Allan Gibbard) to other neo-Aristotelians (Jennifer
Frey, Micah Lott, Chris Toner, James Barham, and Stephen R. Brown).
\newline
\indent My argument is that organic naturalism is more plausible than
social naturalism. I make this case by offering interlocking accounts of
virtue, practical reason, human nature, and nature in general. My case
is intended to be faithful to Foot’s view against McDowell’s, but I also
aim to extend her view. I hope to show that an account can be given of
each theme that is plausible in its own right and even more plausible
considered as a whole.

The Argument
------------

In short, this dissertation defends the thesis that human beings are
best understood as practical, rational primates with a set of natural
ends, including the obligation to acquire virtues and practical wisdom.
I argue that *every* organism has a natural life form and set of natural
ends, where ‘natural’ denotes a property both normatively relevant and
scientifically respectable. What is naturally good for an organism is,
first, to be what it is and, second, to become fully mature. So, since
human beings are natural organisms, it is essential to learn what we are
in order to know what we ought to become. On my account, traditional
virtues such as courage, moderation, and (especially) practical wisdom
belong to ‘the human being,’ where that designation is both descriptive
and normative. These virtues define our human life form and hence define
for us what is to be pursued. Since human beings *are* practical,
rational primates, we *ought* to become practically wise.

The attraction of this view is that we can avoid the twin dangers of
relegating practical rationality and normativity to a non-natural realm
or denying their objective reality altogether. The study of human beings
and the human good is, in principle, open to contributions from
philosophical ethics and the whole family of natural and social
sciences. For example, moral anti-realists can deny natural normativity
but only in the face of biological sciences. On my account, there is a
single definitive criterion by which to judge how successful we and
others are in living a good life: are we becoming what we are?

Chapter Outline
---------------

Chapter 2 defends the thesis that there are such things as natural
normative facts. I give two examples: normative life forms and normative
functions or teleological facts. These “natural norms” may not obtain
everywhere in nature, but they do obtain in all living organisms.

Chapter 3 extends the case to argue that there are *human* natural
norms. I argue that the life form of human beings is best understood as
being practical, rational primates. The natural, normative function of
human beings is to become fully formed, fully mature instances of their
species who can practically reason *well*. Just as we discern what are
normal or abnormal traits of oak trees, wolves, and bears not by making
mere generalizations but by examining *exemplary* members of the species
that are fully grown, healthy, and flourishing, we can discern what are
normal or abnormal traits of human beings by examining exemplary members
of the species – namely virtuous and wise humans.

Chapter 4 describes in more detail what traits count as virtues of
character and practical reasoning. I offer a series of interlocking
features that virtues have, and underscore the importance of practical
reasoning within a “tradition” and culture. And I defend the notion that
the acquisition of virtue is morally obligatory on all human beings
against various misunderstandings and objections.

Chapter 5 returns to the notion of practical reasoning. I provide a more
detailed account of what it means to engage in practical reasoning. I
critique McDowell’s equation of virtue with practical knowledge, in
favor of the distinction between successful practical reasoning (which
is practical wisdom) and rational practices and emotions (which are
organized and managed by practical wisdom, but not identical to it). All
practical reasoners are engaged in a substantive process, not merely an
instrumental one. Success or failure in practical reasoning and rational
practice determines whether one is living a virtuous or vicious human
life.

Chapter 6 defends the foregoing account in light of a renewed discussion
about nature and naturalism. I provide a full critique of McDowell’s
brand of naturalism, which, I argue, is ultimately inconsistent within
itself. As alternatives, I explore two other forms of naturalism:
“unrestricted naturalism” and the Footian form of “organic naturalism,”
and show how the accounts of virtue and practical reason already
developed are compatible with both.

Chapter 7 concludes with a brief summary of the argument and some
reflections on related topics.

A Word About Method
-------------------

I went down to graduate school with a decade-long resolution to write on
Plato’s later dialectic. This dissertation is on ethical naturalism
because Foot’s *Natural Goodness* drew me in a new direction. However, I
still associate her work with Plato’s in at least one way: the
astonishment I felt when first reading Foot’s *Natural Goodness* can
only be compared to my first encounters with the Platonic dialogues –
confusion tempered with delight. So, though my research focus changed,
there remains one respect in which these chapters might be seen as
fulfilling my original resolution to study Plato’s later dialectic – not
by examination but by enactment. That is, I aim to construct the
following argument as a sort of dialogue between author and reader.

I mention this to explain why, for the sake of this project, I have
bracketed discussions of supernaturalism and non-naturalism. Not that
these alternatives do not deserve full consideration, but I take my
primary interlocutors to be readers who share (with Foot) an attraction
to moral realism about virtue but who share (with McDowell) a commitment
to modern science. In order to persuade this kind of interlocutor that
the two are not incompatible, I aim to assume nothing they would not
assume, and to address first the objections that might arise in their
minds. I would have written differently for a different implied
audience, but every dialogue must have a limited scope and a definite
voice. If my study of the Platonic dialectic has taught me nothing else,
it is that one must not only *understand* one’s interlocutors but in
some sense *become* them.

Organic Naturalism
==================

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{Biology cannot, or at least in practice does not, eliminate functions and purposes.}%
{---\textsc{Mark Perlman, \lq\lq The Modern Resurrection of Teleology in Biology,\rq\rq   6.}}
\centering
\end{epigraphs}
While ethical naturalism has a variety of expressions, the common
problem is how to relate ethical and otherwise normative facts with
non-normative facts. The term ‘normative’ refers to ‘ought’ talk. As
Alan Gibbard says:

> What’s special about morality is that it operates in the ‘space of
> reasons;’ it concerns justification and oughts. The term ‘normative’
> is central to much current philosophical discussion. There’s no
> agreement on what this technical term in our discipline is to mean,
> but it involves, in a phrase drawn from Sellars, being somehow
> ‘fraught with ought.’[@gibbard2003normative 321]

So the problem is to explain how the way things *are in fact* relate to
the way things *ought to be*. I shall call this the ‘is-ought gap.’ Hume
is often credited with (or blamed for) the insight that an ‘ought’ can
never be derived from an ‘is.’[^11] When it comes to ethics, how could
mere facts motivate me to act, without any evaluative commitment? How
could mere facts entail some moral truth? How could mere facts *be*
values? As Stephen R. Brown suggests, “when all is said and done, [the
is-ought gap] might be *the* problem of ethics.”[@brown2008virtue 95]
Thankfully, if natural norms exist, then they undercut the is-ought gap.
Natural norms would not “bridge” the is-ought gap; rather, they would
show that the putative gap is spurious.

The purpose of this chapter is to argue that there are such things as
natural norms. At least *some* normativity is discoverable in natural
life forms and functions themselves and that is not projected by human
evaluators. These natural formal and teleological facts are just as real
and familiar as other scientific facts. My hypothesis is that the set of
natural norms includes some human norms which can form the basis for a
plausible ethical naturalism.

The controversy over normativity is an old one and is not likely to be
settled here. My goal, instead, is to present a case that is plausible
to the undecided, and that is sensitive to the concerns of normative
anti-realists (who are zealous defenders of scientific realism) and the
concerns of normative non-naturalists (who are zealous defenders of
moral realism).

Section 1 explains in more detail the two kinds of is-ought gap that
philosophers have taken to render ethical naturalism impossible. It
explains how one notion of natural normativity makes ethical naturalism
at least possible.

Section 2 presents a novel case for what I call “organic normativity.” I
first summarize Philippa Foot’s and Michael Thompson’s case for natural
norms of two types: formal and functional norms. I augment the case on
the basis of generic propositions, that organisms have a real life form
and a natural teleological process.

Section 3 considers the three possible explanations of the phenomena of
natural norms: realist, anti-realist, and reductionist. I show how the
realist is free to accept the simpler explanation. I concede that the
anti-realist has an explanation that is worth exploring further, but
leave it aside since that explanation is not necessarily as attractive
to the scientific naturalist.

Section 4 tackles the alternative to my view that is most popular among
scientific naturalists: reductionism. I aim to show that while
reductionism cannot be fully rebutted, it is, at the very least, no more
scientifically respectable or rationally necessary to believe than
naturalistic, normative realism.

Two Challenges
--------------

Consider a few pretty uncontroversial normative propositions: ‘*better
to be Socrates dissatisfied than a pig satisfied*’ or *‘tolerance of
people with different views is essential to democracy’*. Supposing these
are true, *why* are they true? The non-naturalist has a good
explanation: such propositions pick out fundamental, non-natural, moral
facts. The naturalist anti-realist also has a good explanation: such
propositions express something about the speaker, her individual values,
or cultural norms. The ethical naturalist’s explanation is a bit
trickier. He must show how such statements relate to the *natural*
facts. The most straightforward path would be to argue that “you ought
to be wise” is a normative truth derivable from some other fact that is
natural. In general, ethical naturalism states that some ethical facts
are grounded in natural facts or are identifiable with natural facts.

The is-ought gap has at least five dimensions. There is an *ontological*
gap between normative facts and natural facts; a *logical* gap between
normative claims and non-normative claims; a *semantic* gap between
normative concepts and non-normative concepts; an *epistemological* gap
between the way normative claims are justified and the way non-normative
claims are justified; and a *motivational* gap between how norms
motivate to action and how facts motivate or fail to motivate to
action.[@brown2008virtue 75-6] All these gaps draw the contrast between
bald nature on the one hand – McDowell’s “realm of law” – and
normativity on the other – McDowell’s “space of reasons.” The point is
that when it comes to human evaluations, ‘is’ statements may be
interesting but they seem useless for practical purposes.

To simplify matters, we can use the epistemological form of the is-ought
gap to express the **Is-Ought Challenge:**

1.  If ethical naturalism is possibly true, then descriptive statements
    can serve as premises in arguments with normative conclusions.
2.  But descriptive statements cannot serve as premises in arguments
    with normative conclusions.
3.  Therefore, ethical naturalism is not possibly true.

The first premise of the is-ought challenge sets out a criterion for
ethical naturalism: the normative propositions that feature as
conclusions of ethical arguments must be derived from descriptive
premises. The second premise seems to render hopeless the thought that
we can evaluate things on the basis of what they are. It is difficult to
imagine how the challenge could be met. If it cannot be met, then
ethical naturalism, and neo-Aristotelianism, is a non-starter.

The is-ought gap seems to me fatal to some forms of ethical naturalism.
Namely, it is fatal if we concede that nature is “bald” – a purely
descriptive, mathematical matrix of non-normative facts and laws.
However, the is-ought gap can be *undercut* if we deny that picture.

Of course, I can concede that nature consists of *merely natural facts*.
The concession is a tautology. I do not concede, without argument, that
all natural facts are non-normative. To concede that nature is purely
descriptive would be to allow my opponent to beg the question. My
opponent might likewise complain that I beg the question in my own
favor. It is true that, if I were to merely stipulate that there *are*
natural norms, this stipulation would beg the question in my favor. The
only thing for it is for me to *argue* from agreed upon premises that
there are such things as natural norms. Having done so, it is fair of me
to request an argument to the contrary. If the critic merely insists on
reaffirming that all nature is non-normative, that would be mere
question-begging.

So, are there such things as natural norms? We can use the ontological
form of the is-ought gap to express the **Bald Nature Challenge**:

1.  If ethical naturalism is possibly true, then some natural facts are
    genuinely both normative and natural – there are natural norms.
2.  But there are no facts that are genuinely both normative and natural
    – there are no natural norms.
3.  Therefore, ethical naturalism is not possibly true.

This second challenge, like the first, sets out a criterion that ethical
naturalism must satisfy. Namely, ethical naturalism must offer an
account of some natural norms that are both real and brutely natural,
not derived from other (descriptive) facts.

Foot argues that features of nature are instances of ‘natural goodness’
or ‘natural defect.’ About such qualities, she says:

> …we might equally have been thinking in terms of, say, strength and
> weakness or health and disease, or again about an individual plant or
> animal being or not being as it should be, or ought to be, in this
> respect or that. Let us call the conceptual patterns found there,
> patterns of natural normativity.[@foot2001natural 38]

Two clarifications are required before attempting to meet this
challenge. First, natural normativity is an indeterminate concept that
might include a variety of different kinds of normativity that are not
obviously moral normativity. For example, notions such as the proper,
the healthy, the advantageous, the adaptive, the mature, and so on,
might be genuinely normative without being sufficient as ethical norms.
Even if some natural norms were intrinsic to mundane biological species
such as the white oak (Quercus alba) or the sloth bear (Melursus
ursinus), more work would be needed to argue that natural norms are
intrinsic to the human (Homo sapiens sapiens) and that our ethical life
depends on conforming to them. Secondly, natural normativity might be
only a feature of human nature, as John McDowell argues, or it might be
a feature of any organic life. I shall return to this dispute in later
chapters. For now, I only wish to emphasize that even if natural
normativity can be shown to be plausible, then ethical naturalism is
*possibly* true.

Generic Truths, Natural Norms
-----------------------------

The burden of proof is on the neo-Aristotelian to furnish examples of
natural norms that would undercut the is-ought gap. As it turns out,
there are several plausible ones. The two candidates for natural
normative facts I shall defend are life forms or natural kinds, and
teleological facts or natural function. Although these two kinds of
facts are related, it is helpful to distinguish between morphology and
physiology. The distinction between structures and their functions –
between what natural organisms *are* and what they *do* – is a
distinction between formal and teleological normativity. Both kinds work
for my purposes.

First, start with natural formal facts. Scientists and non-scientists
alike easily observe that nature is full of kinds: sunflowers are not
oxygen; wolves are not bears; lead is not gold; and so on. Kind concepts
allow us to both distinguish x from y and to gather together all the
x’s. Wolves and jackals are both dogs; lead and gold are both elements;
ice and steam are both water, and so on. Classifying entities into
categories and kinds is intuitive and
natural.[@gelman1999biological; @linquist2011exploring] Though I shall
not explore the expansive literature on essentialism, it is prima facie
plausible to affirm that categorial thinking is a constitutive feature
of human thought and possibly a feature of nature itself.

Secondly, scientists and non-scientists alike also observe that nature
is full of end-directed activity. Each thing does its own thing:
sunflowers grow toward the sun; wolves hunt deer and deer flee wolves;
hearts pump blood and eyes see; the sun warms the planet; phytoplankton
oxygenates the atmosphere. Such end-directed processes are
*non-intentional*. Non-intentional processes are sometimes called
‘teleonomic.’[@mayr1992teleology] Teleonomic phenomena may not have a
*director* but they do have a *direction.*

Kinds and their ends can be conceptually distinguished but are
intrinsically related. Is the shape of a hip bone adaptive for its
purpose or is that purpose conducive to the development of such-and-such
a shape? The structural and functional features of organisms are
distinguishable *de se* but not, I suggest, *de re*. Rather than trying
to tease out a distinguish between kinds and ends, we do better to allow
that the natural structures and functions are inseparable aspects of a
single entity. Indeed, philosopher of science Tim Lewens summarizes the
folk biological conception of a “kind” by linking together the concept
of a life form or “essence” with the concept of a function or
“telos:”[^12] a kind is a “teleo-essence,” a thing with an end.

How do philosophers explain the apparent existence of kinds and
teleonomic behaviors? The explanations may be either realist,
reductionist, or anti-realist. Realist explanations argue that kinds and
their ends are what they seem to be: fundamental facts of nature.
Reductionist or anti-realist explanations argue that kinds and their
ends are not what they seem. The anti-realist argues that kinds and ends
don’t ultimately exist; there are only concrete particulars and in
various stages of a mechanical process. The reductionist argues that
*some* kinds exist, but they do not correspond to our initial scientific
categorization; and that *some* end-directed teleonomic processes are
real but it is reducible to non-end-directed processes.

Before discussing these options in full, let’s explore the
neo-Aristotelian treatment of natural normativity in more detail.
Philippa Foot argues that human virtues are instances of a broader class
of natural properties: ‘natural goodness.’[@foot2001natural; cf.
@levy2009philippa] Foot is well aware that her offering is likely to
offend the ears of some listeners. Her defense is the thought (drawn
from Wittgenstein) that crude beginnings are often a necessary first
step on the way to something refined. To earn an audience for her
argument, her first chapter (which she calls a “fresh start”) clears
away some shaky assumptions inherited from Hume and Moore. Many modern
ethicists treat human valuations as unprecedented, almost miraculous,
new appearance in the cosmos. Instead, we should expand the scope of our
inquiry to examine the status of humans as natural entities.

Moore assumed that, in philosophical ethics, ‘good’ is the ultimate
predicate under review. This is one of the “shaky assumptions” Foot
wishes to clear. She argues that statements like “pleasure is good” are
not good paradigms for philosophical reflection. Evaluation of human
creatures and evaluation of plants and animals follow *the same logical
pattern*. In such evaluations, good is good *for*. Contrast ‘good’ with
other predicates like ‘red’ or ‘beautiful.’ In a statement such as ‘the
house is beautiful,’ the predicate ‘beautiful’ doesn’t need a
complement. The house is *beautiful* – full stop. But ‘good’ has a
different logical function. ‘Good’ is more like ‘useful.’ The phrase
‘The house is useful’ *does* need a complement. When we say ‘the house
is useful’ we must specify what it is useful for – *for a mom of six, or
useful for an artist,* or what have you. Likewise, ‘good’ always means
*good for someone* or *for something.* In reference to organisms and
other natural objects, ‘good’ always needs a complement.[^13] If this
crude beginning is anywhere near to correct, we can distance ourselves
from Moore’s starting point and build on another starting point: the
life-form of human beings.

Foot agrees on this point with Michael Thompson’s groundbreaking
work.[@thompson1995representation . Thompson works out the arguments of
this article more fully in his 2008 monograph] Thompson argues that the
concept of “life” is not, as it may seem to some, a property of some
beings where *being* is the fundamental concept; rather “life” is a
fundamental concept.[^14] He says, “Vital description of individual
organisms is itself the primitive expression of a conception of things
in terms of ‘life-form’ or ‘species,’ and if we want to understand these
categories in philosophy we must bring them back to that form of
description.”[@thompson2008life 57] When we observe and examine living
things we rightly employ some shared categories and our conclusions
rightly share a logical structure.

What is that common structure? Thompson reviews and refutes a variety of
crude definitions of life one finds in biology textbooks: life is a
property of anything that is alive, such as capacities to reproduce,
grow, metabolize, etc. The problem is that even though such properties
are co-extensive with the property of being alive, they are wildly
insufficient for the task of *defining* life. Indeed, such properties
depend on a prior understanding of life. Thompson’s alternative is that
life is a fundamental concept. We recognize things as alive before we
learn about their shared traits; indeed, we can only ascribe a set of
traits *living things* share if we are already in possession (absent
that set of traits) of a concept of living things under which we gather
a sample.

On these considerations, it is most reasonable to hypothesize that life
is a fundamental concept, along with ‘being,’ ‘quantity’ and others.
Once we accept that intuitive conclusion, then the argument gets
interesting. For every individual living being is a member of a species
or life-form. And living beings are not just *acted upon*; they *act*.
Each species has its characteristic actions, but the important point
here is that organisms as a whole are characterized by being the source
of their own action. As John Haldane says, quoting the medieval motto:
“things are specified by their power.”[@haldane1998return 262]

Thompson says that “action in this sense is a specific form of *life
process*.”[@thompson2008life 27] Since living beings are characterized
by *acting*, each particular species engages in *its own* particular
activities. Beavers build dams and robins build nests as part of their
own life process. If this is so, then there are life-form specific
*successes* and *failures* to act. Each life-form is subject to its own
normative appraisals: something would be wrong with a beaver that built
a tiny nest or a robin that tried to build a massive dam.

By introducing the term ‘natural normativity,’ Foot is insisting on a
point that is both interesting and controversial. If evaluative
properties like health and disease are really instances of natural
goodness and natural defect, then some evaluative properties are
*primary qualities of nature*. McDowell and others will object to this
characterization of natural normativity. They think it “queer” that
nature should exhibit such properties, and they find it easier to judge
that human beings are the only evaluators. It might be that terms like
‘good’ and ‘bad’ are sui generis evaluative terms, and that evaluative
properties are “in people’s heads” as it were. But Foot’s analysis of
language about plants and animals indicates that such a conclusion is
not the natural presumption.

A much more natural starting point is to assume that such terms are used
relative to natural kinds – and especially life-forms and their
activities or functions. The natural goodness under discussion is not
just a human ascription but seems to be something humans *recognize* in
all living things. Certainly, some properties are human ascriptions
only. Other properties are in the world and only show up in human
ascriptions insofar as we accurately reflect the facts. Foot’s point is
that *some* instances of natural goodness seem much more plausibly
instances of this latter kind. For, there is “no change in the meaning
of ‘good’ between the word as it appears in ‘good roots’ and as it
appears in ‘good dispositions of the human will’.”[@foot2001natural 39]
The identification of what is *good for* a non-human organism is
sometimes identical to the identification of what is *good for* a human
being. Foot’s theory explains this in the simplest way. Foot concludes
that this point holds about “‘goodness’ and ‘badness’ and therefore
about evaluation in its most general form.”

By contrast, McDowell and those who would draw a sharp contrast between
“moral” and “non-moral” uses of the term must give long and
sophisticated explanations for why it makes sense to describe a healthy
plant and a moral person both as “doing well.” The plant is not just
doing well *for my garden* but doing well as itself. It is doing what
such plants are supposed to live. The human being is not just living
well *for a westerner* or *for a Californian* but doing well as a human
being. Rosalind Hursthouse articulates Foot’s insight in this way:

> The starting point is an idea that she has never lost sight of, and
> which figures in her early attack on Hare. It is the idea that ‘good’,
> like ‘small’, is an attributive adjective. What that entails is that,
> although you can evaluate and choose things according to almost any
> criteria you like, you must select the noun or noun phrase you use to
> describe the thing you are calling good advisedly, for it determines
> the criteria of goodness that are appropriate. Hare can call a cactus
> a good one on the grounds that it is diseased and dying, and choose it
> for that reason, but what he must not do is describe it as a good
> cactus, for a cactus is a living thing. He can describe it as a good
> ‘decorative object for my windowsill’ or ‘present to give my
> detestable mother-in-law’, but not as a good
> cactus.[@hursthouse1998virtue 195]

I should make two clarifications about the scope of my thesis thus far.
First, the ‘good’ is a good-of-a-kind, not good simpliciter. It would be
a natural leap to assume that the good-for-us is an instance of the good
simpliciter, but this is a different question altogether. Blackman
argues that there *is* no good other than goods of kinds.[^15] Others
would argue that the good-of-a-kind is an instance of the good
simpliciter. I wish to remain agnostic on this issue. While my thesis
identifies what is good for us as an instance of something *truly good,*
it remains quiet about the broader metaphysical or cosmic significance
of the fact.

A second clarification is this: when I talk of the ‘human good’ I intend
to refer to the species *Homo sapiens sapiens*, the way that talk about
a robin’s egg being *blue* is to predicate a blue-of-a-kind. Folk
ontology tends to classify people by preferences or nationalities akin
to the way it classifies leopards and bears; but my analysis trades on
the concepts used in biology. Hence, my good-of-a-kind analysis is
intended to refer to organisms and biological species, which are most
plausibly understood as natural kinds, rather than social groups, which
are not. There is more to be said about these two clarifications, but
exploring them would take us too far afield.

I would now like to augment Foot’s case with a novel argument for
natural normativity. Like her case, my argument depends on a minimal
commitment to scientific realism[^16] and on “Aristotelian
categoricals.” But I believe the case can be made stronger by utilizing
a feature of language called ‘generics.’

Michael Thompson is one of the first to work out “the special logic of
judgments we make about living things, and then to indicate its
application to ethics.” Such judgments have a variety of names in the
recent neo-Aristotelian literature: the most common are “Aristotelian
categoricals”[@foot2001natural] and “natural-historical
judgments.”[@thompson1995representation; @thompson2008life] Less common
are references to “norms”[^17] or “bare plurals.”[^18] I prefer the
shorter and less adorned term *generic.*[^19]

My postulate is this: **some generics about human beings are true.** If
this is true then, I shall suggest, we have good hope of cutting up
nature at the joints. When combined with a moderate scientific realism,
generic truths from sciences such as biology, physics, and anthropology
(and perhaps others) support a modest natural normativity which will be
further articulated in chapter 4 to indicate how certain traits are
virtues or vices for human beings. The case in brief is this:

1.  If some generic statements describing natural entities are true,
    then some facts are both genuinely natural and normative – there are
    natural norms.
2.  Some generic statements describing natural entities are true.
3.  Therefore, some facts are genuinely both natural and normative –
    there are natural norms.\

Andrew Bailey’s recent paper provides a helpful (and humorous)
introduction to the topic of generic statements. He asks:

> What are generics? A fine question, but a difficult one. Start with
> this sentence: ‘Buddhists are way into meditation’. This first
> sentence is, let us suppose, true. So far so good. But is it
> equivalent to ‘for every x, if x is a Buddhist, x is way into
> meditation’? It does not appear to be. For the second sentence might
> be false (some Buddhists might not be way into meditation) even if the
> first sentence is, as we have supposed, true. The first sentence could
> be true, somehow, even if not all Buddhists are way into meditation
> (similarly, ‘ducks lay eggs’ may be true even if not all ducks lay
> eggs, ‘mosquitoes carry dengue fever’ may be true even if only a very
> few mosquitoes carry that virus, and so on). We are now positioned to
> observe one curious property of generics: they admit of
> exceptions.[@bailey2015animalism 869]

Thus, generics are statements of the form “S is F” or “S has or does F”
where S is not an individual but a class or natural kind. The logical
form of “all S’s φ” does not predicate φ-ing to all members of the
category S without exception, nor does it simply assert that some “S’s
φ,” which is true but uninteresting. For example, consider the true
statement, “wolves hunt in packs” as opposed to the clearly false
statements “every particular wolf that has ever existed has hunted or
will hunt in a pack.” Rabid wolves hunt alone, and injured, or very old
wolves don’t hunt at all. Furthermore, it is true but trivial that *a
large number of wolves hunt in packs*. The generic proposition is a
unique logical expression, neither universal nor particular.

A generic is interesting because it is, or we treat it as, a truth about
forms, or species. The subject of the statement is not all S’s nor
merely some S’s, but the “infima species.”[@toner2008sorts 222. “Infima
species” is the narrowest cut in a genus-species tree, or the most
determinate determinable.] In this way, generics pick out what we might
call formal facts, facts about the life form in question. Thus Sarah
Leslie: “It is widely accepted that [definite] generics are singular
statements which predicate properties directly of kinds. For example,
‘tigers are extinct’ predicates the property of being extinct directly
of the kind *Panthera tigris*, and would be true just in case Panthera
tigris had the property of being extinct.”[@leslie2008generics, section
1.]

McDowell thinks that exceptions to a generic truth are a “logical
weakness” in deriving conclusions from generics about human beings. He
cites the example from Anscombe (and Aristotle) that “humans have 32
teeth,” saying “there is a truth we can state in those terms, but from
that truth, together with the fact that I am a human being, it does not
follow that I have 32 teeth. (In fact it is false).”[@mcdowell1998two
171-2.] McDowell accepts that even a true generic captures fails to
reach deductive certainty. If this is his objection, it rather misses
the point. Aristotelian-categoricals are not half-hearted universal
judgments; they are not universals with widely-acknowledged
counterexamples. Rather, they are judgments of a logically different
kind. Far from being a logical weakness, the ability to capture both a
truth and its exceptions generics are what enable us to capture truths
about natural kinds that help explain statistical variation and
inconsistency.

Prasada says that, “Much of our conceptual knowledge consists of generic
knowledge – knowledge about kinds of things and their
properties.”[@prasada2013conceptual 405] We can approach generics
through what Prasada calls “formal, quantificational” semantics or
through “principled connections.” Principled connections support formal
explanations, normative expectations, and a statistical expectation of
prevalence. In other words, we explain that the dog has four legs
*because* it is a dog (formal explanation); we expect that Fido should
have four legs *unless something is wrong* (normative expectations); and
we expect that if we counted up a population of dogs, *most* dogs would
in fact turn out to have four legs (statistical expectation).

Generic truths, once discovered, set a normative expectation by which we
evaluate individual members on how well or badly they exemplify their
life form.[@prasada2013conceptual 3] The normative expectation cannot,
it seems, be reduced to statistical correlations. Rather, statistical
correlations can be a sign of (or can be an illusion of) a principled
connection.

There is much to be learned about the linguistic features of generics,
but none of the unexplored frontiers render generics useless for
applications in neo-Aristotelian ethics. A few examples of what needs to
be learned include the correlation between statistical prevalence and
normative identity; many generic truths describe what is statistically
prevalent but not all. What is the difference? Is one reducible to the
other? Furthermore, Leslie distinguishes between indefinite generics and
definite generics. For example, “tigers are striped” admits of
specification (“that tiger over there is striped”) while definite
generics do not (“domestic cats are common” does not license “that
domestic cat is common.”) Finally, indefinite generics are trickier:
“Ducks lay eggs” is a true generic while “ducks are female” is a false
one, even though only female ducks lay eggs. And “mosquitoes carry the
West Nile virus” is true even though less than one percent of mosquitoes
carry the virus while “books are paperbacks” is false even though more
than eighty percent of books are paper backs.[@leslie2008generics] How
do we sort through these correlations between generic connection and
statistical prevalence?

These unexplored frontiers represent fascinating puzzles but do not
render generics unsuitable for use in normative and ethical arguments.
Nor should the presence of outstanding questions lead one to believe
generic propositions are confusing or confused. Rather, their normal
acquisition and usage is very familiar, and perhaps inevitable.

Generic truths are acquired via a normal scientific means of empirical
observation, rational reflection, and discussion. This familiar process
is certainly revisable. For example, an ethologist who discovers a wolf
hunting alone may have a normative expectation that the wolf is not
healthy. But she cannot know certainly in advance that this is so. She
must test the hypothesis. A few reasonable interpretations are
available: perhaps the lone wolf is unhealthy; perhaps the initial
generic that ‘wolves hunt in packs’ was false; or perhaps this wolf is
actually a new species of wolf. As it happens, in the case of wolves, no
known species of wolf hunts alone so there is very strong reason to
conclude that a lone wolf is rabid. But the point more generally is that
generics are acquired and modified by a familiar, if complicated,
process of scientific reasoning. Michael Thompson points out that: there
is a “general and thoroughgoing reciprocal mutual interdependence of
vital description of the individual and natural historical judgment
about the form or kind.”[@thompson2004apprehending 52] Put differently,
Micah Lott says:

> At each stage of an empirical investigation, our observations are
> mediated by our current understanding of the life form whose members
> we are observing. At the same time, our observations of those
> individual members will in turn improve our understanding of the life
> form itself, which then makes possible even more accurate and
> extensive future observations.[@lott2012moral 414]

Again, the fact that generic truths are revisable is not a weakness but
a strength of the case I am building. It may be, for all we know, that
penguins can fly (in the air), that some species of penguin can fly, or
that all penguins are really just defective birds. But the most
reasonable belief thus far is the generic truth that penguins don’t fly.
A penguin is not a defective flyer but an excellent swimmer. These
truths obtain in penguins *as a kind* – a biologist or zoologist who
discovered the first flying penguin would become (justifiably) famous
because we would all be (justifiably) surprised. The surprise would not
originate merely from something out of the ordinary – new and
extraordinary creatures, both living and extinct, are discovered every
year. The surprise would originate from the upending of a firmly
established scientific fact.

The first kind of natural normativity I am defending is the mere idea of
a natural, normative life-form. Knowing what a thing is, knowing about
its species or life-form, is to know something descriptive and something
normative about any member of that species. Knowing what a thing is,
furthermore, licenses a range of normative expectations. But we can make
the case for natural normativity stronger. There is another, related
kind of normativity in the natural teleological features of life-forms.
Such natural teleology can also be captured in generic propositions.

To see this second kind of natural normativity, begin with the concept
of a function. Eyes perform the function (in an organism) of seeing,
hemlock trees perform the function (in an ecosystem) of shading rivers,
and so on. Thompson, for example, cites the scientific observation that
“flowers have blossoms of such-and-such type in order that such-and-such
insects should be attracted and spread their pollen
about.”[@thompson2008life 293–94]

While some philosophers of science have thought that teleological
normativity could be explained in terms of function, I would suggest
that the reverse is rather true: the structure of a function is
teleological. There are many senses of the term ‘function,’ but the kind
of biological functions under review are teleological, or at least
teleonomic, in that it is an arrangement of parts toward a particular
purpose or end.

A functional process is not necessarily *willfully* undertaken. But it
does have a beginning, an end (in time), and an end (telos). Clarifying
that functions need not be intentional, we can understand the natural
functions of organisms and organic systems as instances of natural
teleology. James Barham explains the notion of natural teleology in this
way:

> By “teleology,” I have in mind such words and concepts as “purpose,”
> “end,” “goal,” “function,” “control,” and “regulation,” as well as the
> real-world biological phenomena to which these words and concepts
> refer. This means that the word “teleology” should always be construed
> here in its internal or “immanent” sense – purposiveness existing in
> living beings themselves – and never in its external or “transcendent”
> sense of an overarching cosmic principle.[@barham 1]

Ernst Mayr (following Colin Pittendridgh) calls a process “teleonomic”
if it is not a process of intentional purposes.[@mayr1992teleology . Cf.
Colin S. Pittendridgh, “Adaptation, Natural Selection, and Behavior” in
Anne Roe and George Gaylord Simpsons (eds.), *Behavior and Evolution*
(New Haven, 1958), 390-416.] He says, “I have therefore refrained from
using anthropomorphic language, particularly the terms of purpose and
intention, when explaining teleonomic phenomena in animals and
plants.”[@mayr1992teleology 123]

Mayr further distinguishes between teleological (purpose-driven
end-directed processes), teleonomical (non-intentional end-directed
processes in living things) and “teleomatic” (non-intentional processes
in non-living things). A teleomatic process is an “automatic” process
governed by natural law:

> All objects of the physical world are endowed with the capacity to
> change their state, and these changes strictly obey natural laws. They
> are end-directed only in a passive, automatic way, regulated by
> external forces or conditions… All teleomatic processes come to an end
> when the potential is used up (as in the cooling of a heated piece of
> iron) or when the process is stopped by encountering an external
> impediment (as when a falling object hits the ground). The law of
> gravity and the second law of thermodynamics are among the natural
> laws which most frequently govern teleomatic
> processes.[@mayr1992teleology 125]

For my purposes, however, even teleonomic programs would count as
instances of natural normativity insofar as the development of an
organism at one time is incomplete but will later be complete. As
Waddington puts it, “the end state of the process is determined by its
properties at the beginning.”[@waddington1957strategy] Normative, in my
sense, is not the antonym of “descriptive”; normative is the antonym of
descriptive *at present*. “The egg is not a chicken” is true at present.
But “chickens start their life as eggs” is also generically true. Hence
“the egg is a chicken” is a kind of teleological judgment about what it
may, under proper conditions, become. As Chris Toner says,
“natural-historical judgments readily admit of combination into
teleological judgments.”[@toner2008sorts 222]

Taken broadly, then, the first point is to realize that talk about
functions and ends is just as scientific as talk about life-forms,
species, and natural health or disease. Mayr quickly rebuts many of the
common objections (I should rather say prejudices) against teleonomic
processes. For instance, teleological statements and explanations, he
says, do not “imply the endorsement of unverifiable theological or
metaphysical doctrines in science.”[@mayr1992teleology 122] Rather, as
Mark Perlman says:

> Many objects in the world have functions. Some of the objects with
> functions are organs or parts of living organisms… Hearts are for
> pumping blood. Eyes are for seeing. Countless works in biology explain
> the “Form, Function, and Evolution of …” everything from bee dances to
> elephant tusks to pandas’ ‘thumbs.’ Many scientific explanations, in
> areas as diverse as psychology, sociology, economics, medical
> research, and neuroscience, rest on appeals to the function and/or
> malfunction of things or systems.[@perlman2004teleology 1-4]

Mayr’s highly suggestive alternative to conscious purposes is natural
“programs.” A program is “coded or prearranged information” that
regulates an organism’s behavior or development up to a pre-defined
end-point.[@mayr1992teleology 127-8] Mayr’s examples include the
development of bones, organs, and shapes that come with physiological
maturity, migration. Programs are “the result of natural selection.”
However, they contain information: “not only blueprints of the goal but
also the instructions of how to use the information of the blue
print.”[@mayr1992teleology 128] The concept of a program, he assures us,
is similar to concepts deployed by geneticists and computer programmers.
The point is that the telos is not some mysterious spirit hovering above
the organism, beckoning it to reach its full potential but coded into
the organism from the beginning. Regardless of the details of Mayr’s
proposal for explaining teleonomic processes, the mere fact that natural
processes occur is indisputable – and we describe such processes in
generic propositions.

Generic propositions usefully capture the functional or teleological
properties of natural organisms. As Chris Toner says,
“natural-historical judgments readily admit of combination into
teleological judgments.”[@toner2008sorts 222] This kind of combination
of generic truths is very familiar. No sooner have I learned the formal
facts about a penguin (that it is a bird, that it can swim, that it has
a countershaded white belly and dark back etc.) do I learn that
*penguins are countershaded in order to avoid predators from above and
below.*[^20] Since an individual penguin may fail to be countershaded in
the way that expresses its form, it would be defective. This defect is
not a judgment made by scientists and “imposed” as it were, from the
outside, on the penguin. It is rather a normative fact about the
penguin. As Hursthouse says, “Wolves hunt in packs; a ‘free-rider’ wolf
that doesn’t join in the hunt fails to act well and is thereby
defective.”[@hursthouse1998virtue 201]

There is one objection that is easy to forestall. Someone might point
out that genetic drift results in species evolving every which way,
including the emergence of adaptive, maladaptive, and adaptation-neutral
traits. This is true, so far as it goes, but not really an objection.
Two replies are, I think, sufficient. First, it is an inextricable part
of the scientific process to reason out which traits are instances of
natural goodness and which are not. Just because one hundred percent of
organisms eventually die doesn’t mean that death is naturally good for
them. Just because a high statistical number of organisms have a
particular feature – a stripe or a scale or what have you – doesn’t
necessarily mean that the feature is a formal one of the species.
Rather, one must keep an eye open to larger samples, possible
counterexamples, and one must keep one’s generics tentative until they
are very well grounded. Similarly, part of the scientific process is
reasoning out which traits are *adaptive*. Even the way the objection is
phrased assumes that some traits are adaptive – that is, adaptive for
*survival and reproduction.* Allowing even this minimal sense of
normativity concedes my point that the normativity is discovered by the
scientist rather than purely ascribed by him. A second response is that
the generics under discussion are not about
species-qua-fluid-across-millennia but about species-qua-fixed or
apparently fixed within a given period. The fluidity of species over
time, like a slow-motion film with thousands of frames, requires
countless generations. For all we can observe of most species in the
course of a human lifetime (say) or even since the birth of modern
science in the 16th century, the species-at-present are fixed
enough.\newline
\indent In my overall argument, generic truths are intended to serve as
counterexamples to premise 2 of the **Bald Nature Challenge** above.
That challenge asserted that no facts are genuinely both natural and
normative. Generics describe such facts. Generic facts are natural, in
that a large percentage of scientific knowledge consists of scientists
predicating generic truths of natural kinds. Generic facts are also
normative in at least two ways: first, an individual organism may
exemplify or fail to exemplify its life-form; and secondly, *some*
generics pick out natural functional or teleological facts about life
forms (that penguins are counter-shaded *to avoid* predators, that
hearts are *for* pumping blood, etc.). On my view, the most
scientifically respectable option is to accept the straightforward,
generic truths delivered by such sciences as biology and physiology
about forms and functions.

Three Paths Forward
-------------------

My case begins with the indisputable natural phenomena that organisms
appear to exist in natural kinds and, secondly, that organisms engage in
teleological or teleonomic end-directed behaviors. Scientists and
non-scientists can and should attempt to explain these appearances.
There are three possible responses we shall consider.

The first, and most plausible, is to simply accept normative realism. I
call this view ‘organic naturalism’ to distinguish it from an
“enchanted” view of nature wherein even rocks, chemicals, and stars
instantiate normative properties.[^21] While realism about kinds and
teleological phenomena is disputable, it seems to be the simplest
explanation and the one most consonant with scientific realism. When
Kant denies realism about natural teleology he admits we cannot help
acting as if it were true.[@huneman2006naturalising] If we cannot help
acting as if p were true, it seems a fine hypothesis that p is, indeed,
true.

The second, and least plausible, path is that we could embrace
full-scale normative anti-realism and deny the objective reality of any
such norms in nature (and indeed, even in human beings). This path
requires us to explain away all putative natural kinds and teleonomic
phenomena in nature. (It might also require explaining away practical
reasoning and intentional, end-directed action in human beings.) For
example, we would have to deny that animals, plants, insects, all living
things (and even ecosystems) exhibit end-directed or teleonomic
behavior: eyes see, hemlock trees offer shade to fish, stomachs digest,
deer leap to avoid predators. This denial is almost incredible. If all
generics are false (or only conventionally true) then it is in some
important sense false that ‘wolves hunt in packs’ and false even that
‘penguins are birds.’ It is false not only that “eyes see” but even that
“humans are primates.” Arthur Ward draws this conclusion:

> Perhaps the most provocative conclusion of the dissertation is that
> there is no such thing as good eyesight or bad hearing *per se*. Or
> equivalently, that it is strictly speaking false (without further
> qualification) that humans have ten fingers and ten toes. Both sorts
> of claims rely on teleological norms that entail good-of-a-kind
> evaluation, the application of the attributive “good,” which I argue
> can only be legitimately applied to artifacts… some people find the
> denial that “humans have ten fingers” or the possibility of “good
> hearing” to be so implausible as to be a reductio of my entire
> argument.[@ward2013against 82]

Denying the existence of (normatively significant) good eyesight does
indeed seem to me a reductio of such anti-realism. Even if a position is
‘absurd,’ that doesn’t mean it is automatically false or not worth
considering. It might well be true. But if it is true, then absurdity is
true and truth is absurd. There have been many philosophers who have
thought so. Despite my inability to see the plausibility of global
normative anti-realism, I must acknowledge that it has impressive
defenders who deserve a fuller response than I can give here. Since
anti-realism is not likely to appeal to the scientific naturalists in my
intended audience, for present purposes, I shall proceed on the
assumption that modern scientific reasoning is capable of grasping the
non-absurd intelligibility of nature.

The third path, and the most plausible rival to realism, is to develop a
reductionist account of apparently natural norms. This path accepts the
appearance of such things as natural kinds, natural teleology, natural
functions, etc., but *reduces* these phenomena to less spooky (read:
more mechanistic) phenomena consistent with a conception of bald nature.
For this section, I ignore natural kinds and focus simply on
teleological normativity. So we can call reductionism of such natural
norms “teleological reductionism” or “teleoreduction,” following James
Barham.[^22] Arguing for or against teleoreductionism has become a
cottage industry.[^23]

I find the fervor for reductionism in philosophy of science and
philosophy of mind odd. Perlman is right to be surprised. He says: “It
is surprising that analytic philosophers, with their strong focus on
science, would reject a notion that is so central to some areas of
science, most notably, biology and engineering sciences… Biology cannot,
or at least in practice does not, eliminate functions and
purposes.”[^24] I do not think that the appeal of teleological
reductionism is due to its intrinsic plausibility; its appeal is mainly
due to the mistaken assumption that it is the only scientifically
respectable option. When compared with another view that is equally
scientifically respectable and more plausible, that appeal wanes.

Nevertheless, the arguments for teleoreductionism are sophisticated, and
some proponents hold out hope for even better arguments to come. More to
the point, some of its proponents affirm reductionism because of an
operating background belief that, globally, reductive physicalism is a
victorious view, despite ongoing local skirmishes. My objections to the
reductionist argument, which amount to the charge of non-sequitur, are
unlikely to overturn someone’s background beliefs. Barham’s summary of
the dialectic seems to me correct:

> If someone were comfortable with a purely physicalist worldview that
> had no place in it anywhere for teleology in any form, then nothing I
> will say here would do much to discomfort that individual. All I claim
> is that, if one is already convinced of the rationality of taking at
> face value at least some of the teleological concepts that we employ
> both in everyday life and in biological discourse, then one is not
> required to relinquish that conviction on the basis of the notion that
> molecular biology and the theory of natural selection, either
> severally or jointly, have already settled the matter by providing us
> with a successful means of eliminating such concepts from
> biology.[@barham 110]

I am content to defend the claim that naturalistic teleological realism
(and more broadly normative realism) is a live option even for the
non-reductive scientific naturalist. Hence, the remainder of this
chapter will examine some reasons for preferring realism to reductionism
when considering normative realism in isolation, even if these reasons
are not enough to overcome someone’s background commitment to the
contrary.

Against Reductionism
--------------------

First, what would it mean to “reduce” teleology? Barham’s definition of
teleoreduction, which I find adequate to my purpose, is this:

> To reduce a putative teleological phenomenon is to give an account of
> the phenomenon that is both empirically and theoretically adequate and
> that neither employs any teleological concepts nor presupposes any
> other teleological phenomena.[@barham 109]

The two primary candidates for teleoreduction are causal-role reductions
and natural selection reductions. Causal-role or causal-contribution
explanations (endorsed by Donald Davidson, Robert Cummins and others)
reduce teleological relations such as “in order to” and “for” and “to
the end of” to bare cause-effect relations. For example, the function of
the heart is defined in reference to its role in the oxygenation of a
vertebrate’s blood.

Barham summarizes causal-role positions in the recent literature on
teleological and natural functions:

> The first position, stemming from a seminal article by Cummins (1975),
> views being a function fundamentally as making a causal contribution
> (in the efficient-causal sense) to the maintenance of a larger system
> of which the function in question is a component part.[^25]

In that seminal article, Cummins attacks the assumptions that “(A) The
point of functional characterization in science is to explain the
presence of the item (organ, mechanism, process or whatever) that is
functionally characterized,” and “(B) For something to perform its
function is for it to have certain effects on a containing system, which
effects contribute to the performance of some activity of, or the
maintenance of some condition in, that containing
system.”[@cummins1975functional 741] Essentially, this path explains a
natural function as a relation between parts and wholes.

The natural function is not reducible to just any relation, nor even to
any *causal* relation, for there are many part-whole relations that are
obviously not functions. For example, the heart is not just the
blood-circulating part of the human body; it is also the “thumping
sound” part. Heartsounds and circulation are both effects of the heart’s
beat. It is obvious, however, that making heartsounds is not the
function of the heart, but (at best) a side-effect of performing its
function. So the question is how one can determine *before identifying
the function* exactly which part-whole relation is the functional one?

It does no good to assert that part A has a causal role within organism
B *after one has already presupposed an irreducibly functional
analysis*. The teleoreductionist is obliged rather to show how one can
distinguish teleological and non-teleological part-whole relations in
absence of or prior to such presuppositions. The teleological realist
also affirms that hearts play a causal role in the vertebrate’s body.
The teleological realist’s point is that the heart is a part of the body
with an irreducibly functional part. It is simultaneously true that the
heart *causes* blood circulation and that the heart pumps *in order to*
circulate blood. The heart is *the blood pump* of the body.

The teleological realist is free to identify the function of a
particular body part, and then to characterize the part-whole relation
in irreducibly functional terms; the teleological reductionist cannot do
likewise. Relatedly, we should note that even the reductionist’s notion
of a “role” is essentially teleological. The thought that the heart
“plays a role” within the organism’s circulatory system seems to be
conceptually identical to the thought that the heart *has a function*
within the circulatory system. So the reductionist must be wary not to
smuggle in teleological concepts into a putatively non-teleological
account. If all available reductionist strategies *did* somehow smuggle
in teleological concepts, this fact would be somewhat telling. One
cannot be blamed for wondering if reduction is not just difficult but
impossible.

The second major candidate for teleological reduction is the
“natural-selection” strategy which appeals to the historical genesis of
the organ in question. This reductive strategy is perhaps best viewed as
a supplement, rather than alternative, to the causal-role strategy.
Natural selection reductions provide a causal-historical explanation of
a present day teleonomic function.[@millikan1989defense] There are a few
different sub-strategies on this front.

One sub-strategy argues that *natural selection itself* is a teleonomic
or quasi-teleological process that can produce organisms with functional
properties. How exactly does this work? We first define survival and
reproduction as the goal-state of organisms (however this came to be);
then, we distinguish effects that tend toward the organism’s survival
and reproduction from those that do not or those that are irrelevant to
that end. Circulation contributes to survival and hence is a more
plausible candidate for the heart’s function than making heartsounds.
Simply put, we can describe the present state of the heart (including
its causal-role in bodies) by referring to its historical genesis: the
heart evolved *because* it tended to the survival of certain kinds of
organisms.

My objection to this sub-strategy is this: have we even produced the
*right kind of explanation* for a phenomenon such as the pumping of the
heart? Obviously, natural selection is not a *selection* in the sense
that *some agent* is “selecting.” Natural selection is rather a
scientific description of a process wherein generations of populations
are either extinguished or preserved. Natural selection comes in to show
how the organism varies, passes on heritable traits, and gives rise to
new phenotypes. Thus Barham says:

> …the functionally coordinated organism must already exist before it
> can be selected. On this view, we assume that the functional
> coordination of the organism is *prima facie* evidence of teleological
> determination, and since that functional coordination is presupposed
> by the theory of natural selection, the theory is in no position to
> reduce the apparent teleology in biology to mechanism.[@barham 125]

So much is clear in outline. However, the details of the case are
philosophically important. Specifically, natural selection explains
heritable traits that (i) varied in the past and which (ii) played a
role in the reproductive rates of the population.[^26] Natural selection
is not supposed to and does not explain the bare existence of an initial
population. Rather, the initial organism or population – with a complete
set of formal and functional traits – is taken for granted. So the worry
is that the process of natural selection is not the *right kind* of
explanation to serve as a candidate for the reduction of apparently
teleological activity within individual organisms.

When we are wondering how or why it is that the heart seems to have a
definite function (to circulate blood) that is discernible from other
side-effects (to make heartsounds), the question is about organismic
behavior in general. Chemicals and compounds do not grow and develop and
perform characteristic activities in the structured way that organisms
do. My answer is that such normativity is a fundamental natural feature
of organic life, a kind of brute natural law discovered a posteriori by
the scientific method. The natural selection reductionist’s answer is
that the teleonomic function of hearts emerged out of a long history of
phenotypic variation. My question is: so what? Mechanistic forces that
are taking place between a population and its environment (droughts,
famines) or within a population’s genetics (genetic drift, normal
reproduction) are compatible with parallel teleological forces. Indeed,
Barham suggests that the burgeoning field of evolutionary developmental
biology might be able to supply some of the connections between these
two kinds of processes. He calls “phenotypic accommodation” the distinct
process of “inherent compensatory or adaptive capacity of organisms” –
or simply homeostasis.[@barham 131] The scientific hypothesis some are
investigating[@shapiro2009revisiting] seems to be that these two
processes are separately necessary but only jointly sufficient causes to
explain the presence of a trait (like pumping hearts) in a population.

A second popular sub-strategy with natural selection reductions is that
of Ruth Millikan.[@millikan1984language] Millikan argues that a “proper
function” by definition refers to an object’s empirical history. She
says that “definition of ‘proper function’ looks to history rather than
merely to present properties or dispositions to determine
function.”[@millikan1989defense 289] A function is a “recursive”
concept, since the function of a present day organ is defined in
reference to ancestor’s functions; and “non-historical analyses” fail in
important ways. Barham summarizes Millikan’s definition of a proper
function: “a present trait’s being a function [is] equivalent to its
having been naturally selected due to the fitness advantage conferred on
an organism by the physical effects of the ancestral trait of the same
type from which the present trait-token is descended.”[@barham 9]

The idea here is that ancestral organisms had such-and-such phenotypes
which conferred hearts upon present-day vertebrates after many
generations of reproduction. A consequence of Millikan’s view is that an
organism’s “proper function” simply cannot be read off its present
capacities; we can’t just observe that hearts *seem to be for
circulating blood* and infer from this observation that they are,
indeed, for circulating blood. Rather, the proper function of a
(present-day) heart can only be identified by its empirical history.

Millikan’s view entails a implausible corollaries. First, suppose we
discovered a new heart-like organism, say of extraterrestrial origin
with distinct evolutionary parentages. It would have to be classified as
having a different proper function, despite the fact that it circulates
oxygenated blood through the organism just like terrestrial hearts.
Secondly, hypothetical “Swampman” arguments press a similar point.
Suppose an exact material replica of Donald Davidson spontaneously
emerged from a swamp; on Millikan’s theory, even though the Swampman is
equipped with a heart and lungs and legs and eyelids, none of these has
*any* “proper function.” Millikan bites the bullet on both of these
implausible corollaries:

> Take any object, then, that has a proper function or functions, a
> purpose or purposes, and consider a double of it, molecule for
> molecule exactly the same. Now suppose that this double has just come
> into being through a cosmic accident resulting in the sudden
> spontaneous convergence of molecules which, until a moment ago, had
> been scattered about in random motion. Such a double has no proper
> functions because its history is not right. It is not a reproduction
> of anything, nor has it been produced by anything having proper
> functions.[@millikan1989defense 292]

On Millikan’s view, then, such an organ with an identical structure that
causes identical effects would not have any “proper function” at all.
Millikan is well aware of the seeming absurdity of this conclusion, and
defends her view against wild hypothetical counterexamples.
Nevertheless, it still seems to me the counterexample cuts against her
view, despite being fanciful.

It is more plausible, in light of such counterexamples, to accept the
thought that an organ’s *function* and its *historical genesis* are not
identical. We can support this intuitive conclusion by showing a few
ways that the two concepts come apart: Useless vestigial organs have an
empirical history but no present day functional capacity; spandrels have
a present-day functional capacity with no direct, primary selection
history; the language capacities in say, the right hemisphere of the
brain *can* be taken over by the left hemisphere in the case of injury
or lobotomy, presumably because the brain is (present-day) adaptable and
not because the brain function redundancy was selected for in every
individual case. These counterexamples demonstrate *at least* that
function and history conceptually can come apart.

What is the alternative? In Barham’s view, functions are “essentially
modal, not historical, concepts.”[@barham 139] Barham quotes Fodor’s
vivid statement that “my heart’s function has less to do with its
evolutionary origins than with the current truth of such counterfactuals
as that if it were to stop pumping my blood, I’d be
dead.”[@fodor2001mind, 86-7; cited in @barham 138.] If we made contact
with extraterrestrials whose blood-like liquid was circulated by a
pump-like organ, how could we discern whether it was a heart? We could
query about the historical genesis of the organ on that planet, but we
would first rightly query: *what would happen if that organ stopped
pumping?* If the Alpha Centaurians, too, would die without the beating
of that organ, we would justifiably call the organ a ‘heart’ even though
it had a very different history.

Barham cautions against “imagining that ‘selection history’ could confer
normative value on a biological function in the same way that pedigree
confers value on a horse, or provenance on a painting.”[@barham, 140.]
“History” is not a special power but is simply the set of physical
interactions over time. The question about which set of physical
interactions over time produced X might be (and I think is) intimately
related to questions about the function of X; the point is that they are
two different questions. Michael Thompson, too, insists that judgments
about natural teleology are made true from the form of life under
question, not from “hypotheses about the past.”[See
@thompson1995representation 293. Christopher Toner adds that judgments
about natural teleological facts are made true regardless of the origin
of the facts, “whether about creation or natural selection” (“Sorts of
Naturalism,” 223).] This seems right to me. It does not matter for
present purposes *how* the function came to be, just whether or not it
really *is* at present. Barham is right to point out that the problem
with Aristotle’s views of biology (say, believing that the seat of
perception was not in the brain) was not that he lacked knowledge of
evolution, but that he lacked an adequate knowledge of physiology.

My conclusion, based on these considerations, is that reductionist
strategies are not very promising. ‘Not very promising’ is a far cry
from ‘hopeless.’ There may be a successful reduction *one day*. But
today is not that day. It may turn out to be possible to find an
explanation of teleonomic phenomena “that is both empirically and
theoretically adequate and that neither employs any teleological
concepts nor presupposes any other teleological phenomena.” Until then,
the scientific perspective of empirical biology conforms most closely to
the commonsense conclusion that *hearts are for pumping blood.*

Part of the resistance to this conclusion is a deeply-rooted anxiety
about the prospect of accepting naturalistic normative realism whole
cloth. Teleological realism in biology fell into disfavor about the same
time as Francis Bacon declared that the search for final causes
“defiles” science.[^27] This anxiety is misplaced. The proper reply to
Bacon is that the teleological nihilism hypothesis has been tried and
found wanting. Modern science is no less teleological than it was in the
17th century; perhaps even more so. Fitzpatrick says that, “While
neo-Darwinian evolutionary theory does soundly reject any appeal to
teleology in the process of evolution itself, there is a large
literature in contemporary philosophy of biology defending the
legitimacy of employing teleological concepts in connection with
adaptations.”[@sepmoralitybiology .] Thomas Nagel’s recent philosophical
defense of scientific, Darwinian, natural teleology received wide
criticism.[@nagel2012mind .] However, one critical view by Michael
Chorost pointed out that Nagel’s main error was not in defending
naturalistic teleology but failing to cite the *existing scientific
literature*:

> Natural teleology is unorthodox, but it has a long and honorable
> history. For example, in 1953 the evolutionary biologist Julian Huxley
> argued that it’s in the nature of nature to get more advanced over
> time. “If we take a snapshot view, improvement eludes us,” he wrote.
> “But as soon as we introduce time, we see trends of improvement…”[^28]

In addition to Huxley, we can point to Arnhart’s persuasive argument
that teleology is an irreplaceable assumption in medical
science,[@arnhart1988 .] or Zammito’s defense of the ongoing relevance
of natural teleology in biology, since organisms seem to be
intrinsically purposeful.[@zammito2006teleology .] Darwin himself might
have been a teleologist.[@lennox1993darwin; @lennox1992teleology .] And,
as Stephen Brown argues, “Neo-Darwinism… can actually be seen as
underwriting teleological explanations in biology, that is, as playing a
crucial theoretical role in explaining certain kinds of telic
phenomena.”[@brown2008virtue 109] I have not done anything to place my
account on neo-Darwinian footing; instead, my aim is to rebut the charge
that finding such a footing is unthinkable. While natural teleological
realism is still controversial, it is not a controversy between
philosophy and science but a controversy *within science*.

Conclusion
----------

The goal of this chapter has been to argue that there are such things as
natural norms. The naturalistic normative anti-realist and the
non-naturalistic normative realist agree that all natural facts are
non-normative facts. This gives rise to the is-ought gap as a matter of
logical necessity. But the is-ought gap might simply turn out to derive
from an obsolete view of nature that cannot account for biological
science, let alone the social sciences. The neo-Aristotelian view of
natural normativity does not *bridge* the much vaunted is-ought gap but
rather undercuts it. Natural norms serve as counterexamples to the
common belief that all natural facts are descriptive (non-normative)
facts.

Instances of natural normativity include familiar scientific facts about
organisms: they bear a life form and they engage in natural teleological
processes. The three possible responses to such putative natural norms
are to accept them (as I have recommended), reject them, or reduce them.
Conceding to global normative anti-realism would require adopting
scientific anti-realism as well, which is a formidable philosophical
view I have not attempted to consider here. Scientific realists tend to
choose a reductive strategy, but I have given reasons to think reduction
has not yet been accomplished and is not likely to be accomplished in
the foreseeable future. In the mean time, it seems clear that
naturalistic normative realism is not only assumed to be true in
everyday scientific inquiry but is also commended by philosophical
reflection.

The argument thus far has attempted to demonstrated that it is at least
*possible* that ethical naturalism can derive normative human ‘oughts’
from other, basic, natural ‘oughts.’ The next chapter aims to
demonstrate that it is *plausible*.

Practical Primates
==================

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{When we are investigating what the good life is... and how living virtuously might achieve it, we are aided by investigating our human nature. This in turn we do by seeing how we humans are a part, though a distinctive part, to the world that the sciences tell us about.}%
{---\textsc{Julia Annas, \lq\lq Virtue Ethics: What Kind of Naturalism?\rq\rq 11.}}
\centering
\end{epigraphs}
If all natural organisms can be described by normative generics, and
humans are natural organisms, then humans can be described by human
generics. If statements such as “apple trees produce apples” are norms
capturing the object’s natural end, then perhaps statements such as
“human beings become knowledgeable” can capture our natural end. Perhaps
such statements can be both normative and descriptive natural norms
applicable to humans – or simply *human norms*. These natural norms
would be binding on human beings as practical rational animals and not
merely invented by human individuals or human cultures. These norms
would be natural without being crassly biological; they would be both
biological and practical.

The purpose of this chapter is to propose that there are such things as
human norms. The strategy for identifying them is fairly simple: we must
uncover generic propositions about human beings that are both
scientifically true *and* normatively significant. For example, we need
the same type of Aristotelian Categoricals or generics formulated in the
previous chapter about flora and fauna. We need generics to answer
questions like: what is a human being? All else depends on the life form
of our species. Also, what kinds of activities does “the human” being
do? What kind of life does it live? What is its natural end, if it has
one – or what are they? The answers would be both descriptive and
normative. Human norms would provide prima facie normative bindingness;
if I am a human being by nature, it would be initially binding upon me
to *do what humans do* and *become what humans become*. These human
norms, I shall suggest, give us insight into the concepts of virtue,
excellence, wisdom, and flourishing. For example, it might be that some
normative propositions such as “you ought to be wise” are brutely
normative *natural* facts.[^29]

Section 1 begins with the observation that human beings are natural
organisms. Nevertheless, human beings are animals of a peculiar sort who
engage in such activities as speaking, innovating, deliberating, and so
on. So, I conclude, human beings are practical, rational primates. This
conception of human nature is seamlessly both normative and descriptive.
If humans fit the larger pattern of natural normativity defended in
chapter 2, then evaluation of individual human beings is possible by
comparison to the human life form.

Section 2 attempts to sympathetically articulate and respond to a few
critical objections philosophers have had about the neo-Aristotelian
project of grounding ethical evaluations in a normatively loaded
conception of human nature. Each of these receives an initial rebuttal,
though a few of them will require further comment in chapter 6.

Section 3 begins to apply the foregoing account of human nature and
natural human norms to ethics. Specifically, I shall argue that as
practical, rational animals, a basic human norm is that one *is to
become a fully mature human being*. Practical primates have a prima
facie normative obligation to be what they are (to respect the
conditions and criteria of their life form) and a prima facie obligation
to become fully mature practical primates.

Animals of a Peculiar Sort
--------------------------

The previous chapter drew substantially from Philippa Foot to argue that
*any* animal exists within a nexus of natural normativity. Since humans
are animals, it would seem to follow that humans are subject to natural
norms. Foot is well aware that the derivation of normativity from brute
nature is likely to seem absurd, especially when it comes to human
beings. She says:

> The idea that any features and operations of humans could be evaluated
> in the same way as those of plants and animals may provoke instant
> opposition. For to say that this is possible is to imply that some at
> least of our judgements of goodness and badness in human beings are
> given truth or falsity by the conditions of human life. And even if it
> is allowed that certain evaluations of this kind are possible – those
> vaguely thought of perhaps as ‘merely biological’ – there is bound to
> be skepticism about the possibility that ‘moral evaluation’ could be
> like this.[@foot2001natural 38.]

Despite such legitimate worries, we have followed Foot in trying to earn
a hearing for this notion by arguing that the meaning of ‘good’ in
so-called ‘moral contexts’ does not have a special logic of its own.
Rather, ‘good’ and ‘defective’ pick out natural properties of living
things. The goodness of a cactus is relative to its cactus nature;
likewise, we should expect that the goodness of human beings is relative
to their human nature.

Are human beings natural organisms? On its face, calling human beings
organisms or animals or primates appears to be an innocent truism. *Of
course* humans share properties in common with every other organism:
they enjoy a particular evolutionary history; they move about the earth
engaging in activities such as reproducing, sleeping, feeding, dying,
and so on. But some have objected to the suggestion that human beings
are *mere* animals. We are different from other animals, and the
significance of this difference is a matter of some controversy.
Certainly, humans exhibit a range of actions such as language and
complex social systems that other animals do not. As Hursthouse
summarizes:

> When we moved from the evaluations of other social animals to ethical
> evaluations of ourselves, there was an obvious addition to the list of
> aspects which are evaluated. The other animals act [as opposed to
> chemicals which are only acted upon.]. So do we occasionally, but
> mostly we act from reason, as they do not, and it is primarily in
> virtue of our actions from reason that we are ethically good or bad
> human beings. So that is one difference that our being rational
> makes.[^30]

In light of the difference of being rational, the task in discovering
true generics about human beings is capturing what is common and what is
unique about humans.

My view is that human beings are animals of a peculiar sort where the
peculiarities do not eliminate the commonalities. The traditional
formula that humans are “rational animals” is close to correct. As such,
both the *animal* part of that formula is essential and the *rational*
part. To see why, let’s first consider in a bit more detail what it
means to be an animal, and why it matters. Then we shall look at what it
means to be the peculiar sort of practically reasoning animal that we
are.

To be an animal is to belong to the “tree of life” – and to have a
location in the broader story of life on earth.[^31] That story begins
3.5 billion years ago with the first living organisms, and our own part
begins about 200,000 years ago with the emergence of anatomically modern
humans. In the contemporary classificatory scheme, we can locate humans
within the phylum chordata, the class mammalia, the order of primates,
the suborder haplorhini, the familiy hominidae, the genus homo, and the
species homo sapiens.

Does this matter ethically? I think it can be demonstrated that the
common history of living organisms (including humans) is not ethically
irrelevant. At the very least, the bundle of properties intrinsic to our
animality serves as a condition of our ethical life. At the most, our
animality is (sometimes) a *criterion* of our ethical life.

One example that will suffice to illustrate the point is mortality. As a
matter of plain scientific fact, we are mortal – like every other living
organism or species. All life on earth undergoes a process from a humble
beginnings in a single cell through infancy, maturation, and adulthood,
at which point it may reproduce itself before dying. All of these phases
we notice in human animals as well. The human life cycle is
characterized by various phases, including growth, language acquisition,
puberty, physical maturity and characteristic activities, aging, and
death.

Now, all that is good in life depends on the prior state of being alive
at all. Although death is “normal” at the end of the life cycle, it is a
very basic normative fact that being alive is a good. What is so morally
heinous about murder is that it unjustly and prematurely destroys the
good of life. Where theft robs one of this or that particular good,
murder robs one of life which is the condition of all other goods. In
this way, mortality is a condition of ethical life; prima facie, one
ought not behave in such a way as to make others die (or to put others
at risk of dying) before their life cycle is complete.

My point is not that the status of mortality is uncontroversial. Whether
mortality is condition or criterion of ethical life is a live
controversy in bioethics: should we attempt (if possible) to overcome
mortality?[@bostrom2005transhumanist; @bostrom2005defense] Would doing
so be a morally innocent intervention like body-building or a morally
loaded intervention like genetically modifying embryos? My point is that
being mortal creatures whose very life is a fragile homeostasis is *at
least* a condition that must be taken into account when living life or
constructing an ethical theory.

What other conditions of animality are possible criteria of ethics? The
whole range of facts that characterize a human being and a human pattern
of life. When I say “pattern of life” I do not just mean the crudely
biological features of life; I mean the whole range of biological and
neurophysiological facts by which a human being undergoes the process of
living from birth to death.

We cannot, except via abstraction, describe the human species adequately
without describing biology, ethology, psychology, and sociology. For
example, it might seem a purely descriptive biological trivium that
humans have 23 chromosomes in each somatic cell. But genetic defects in
a person have enormous effects on that person’s quality of life and on
the community in which he lives. Apparently innocent “descriptions” of
human animals are inseparable from ethological and anthropological
descriptions, which which are both descriptive *and* normative.

Furthermore, a scientific account of humanity cannot leave out that
humans have large brains relative to other primates, with a neocortex
and prefrontal cortex that correlate with abstract thinking, problem
solving, society, and culture. A scientific account cannot leave out
that humans don’t just suffer physiological responses like fear and
excitement or arousal, they willfully seek out such emotions for
themselves through art and entertainment and willfully cause them in
others. Presumably, even an alien anthropologist who knew nothing of
human language or “what it is like to be a human” would be able to
notice, upon examination, that a human’s laugh or cry is different from
a hyena’s laugh or a crocodile’s tears. Part of the alien
anthropologist’s examination would be to examine the body, brain, and
hands of human beings. One of the first things we can imagine they would
notice is that humans live in cultures and societies. They are not
merely “social animals” like apes; they are language-users,
communicating in signs and symbols. Their language is an extremely
complex, open-ended system which is both recursive (able to nest
propositions within propositions) and productive (able to create
sentences by potentially limitless combinations of words). In virtue of
language and their opposable thumbs, they are creative; they don’t just
live on the ground or under ground, but build houses and shelters,
sometimes in new places, such as caves, trees, hills, mountains, etc.
Also, they are self-reflective. They establish social relations upon
biological grounds (some children growing up with natural parents) and
upon normative grounds (some orphans growing up in orphanages created by
philanthropists). Even before introducing the “human” point of view, we
can describe “the human” form of life in some detail. My hope is that
these generics are plausibly knowable from an “objective” or
third-person point of view of scientific exploration, data gathering,
inductive generalization. They seem to have at least *potential* ethical
significance; even so, the most ethically significant fact about us is
the peculiar differentia of our species: practical rationality.

It is now time to offer a first characterization of the ‘practical
reasoning’ of an organism.[^32] Practical reason occupies a place of
importance in the theories of many virtue ethicists. For example, Foot,
McDowell, and MacIntyre have each treated the theme.[^33] Chapter 5
focuses on the neo-Aristotelian accounts of practical reasoning in some
detail. For now, I shall only offer an initial exploration. Jay Wallace
gives an adequate general definition of practical reason: “Practical
reason is the general human capacity for resolving, through reflection,
the question of what one is to do.”[@seppracticalreason, introduction]

When we take a wide view and observe human behavior in the context of
other animal behavior, observing ourselves both “from inside” and “from
outside” the human perspective, we notice a range of properties not
shared by other mammals: grammar and language, fire-making, cooking,
sexual union for pleasure, abstract reasoning, science, philosophy,
religion, mythology, and agriculture. Is there any way to collect these
idiosyncrasies into one or a few generic categories? All of them depend,
in one way or another, on activities we call “rational.”

Predicating rationality is not merely based on the fact that “some
people can do sums,” as Bertrand Russell joked.[@russell1992basic 73]
Rather, we predicate rationality on the basis of observing a range of
activities such as: to observe, reflect, and perceive; to remember,
predict, and categorize; to decide, determine, and pursue; to abstract,
explain, and infer; to criticize, blame, and praise; to admonish,
prohibit, and command; and so on. Abstracting to what all these
disparate activities have in common gives us a sense of what the generic
activity of practical reasoning is.

Practical reasoning is the process of self-determining, of taking our
actions “into our own hands” so to speak. Some of the above rational
activities are intrinsically aimed at action, while others are not. But
even the theoretical activities (like reflection) can be and are put to
use in practice. Hence, on my view, practical reason is constituted by
at least four capacities that in turn constitute human nature: the
capacity to speak, to live in society, to engage in rational practices,
and to create or innovate. Let’s consider each of these four properties
in turn.

First, we should consider the unique phenomenon of human language.
Aristotle observed that, “Man alone of the animals possesses
speech.”[^34] Other animals have forms of communication and even a sort
of speech. But nothing in modern science has superseded or contradicted
the observation (obvious to anyone) that human speech is qualitatively
different from other animal speech. Modern science *has* helped us to
understand exactly what is different. Upon reflection, researchers have
observed communication systems used by other animals such as bees or
apes are closed systems consisting of a finite, usually very limited,
number of possible ideas that can be expressed. In contrast, human
language is open-ended and productive, meaning that it allows humans to
produce a vast range of utterances from a finite set of elements, and to
create new words and sentences. Our language is unique: it is
grammatical, open-ended, recursive, and productive. We are animals who
use signs and symbols to communicate self-reflective and abstract
thought.[@deacon1998symbolic]

Speech is inseparable from self-reflectivity and sociality. Through our
animal senses comes a sensitivity to our surroundings, the ability to
see the world, ourselves, the sun and stars, to hear our fellow
creatures, and to take the whole cosmos into consciousness. Before
learning to speak, infants lack the cognitive capacity to understand
what pours in through their senses. Infants also do not initially grasp
the difference between non-human and human speech, but learn words by
imitation just as well as they learn tweets, barks, and growls. Once
words are recognized and learned, an irreversible change occurs. Through
speech comes a whole second cosmos of culture. Through speech comes
intentionality in all its forms. Through speech comes practical
communication (i.e., “pass the salt”), and whole languages and cultures
(about 5,000 distinct languages). Through speech comes
self-consciousness (“who am I?”), abstraction (“all grass is green”),
science, philosophy, religion, mythology, technology and more. Even art
and music, arguably, arise from the rational capacity to direct our
actions to create not only what instinct demands but whatever the
imagination can invent.[@orians2008nature . Orians says that “Americans
spend more money on music than on sex or prescription drugs.”]

The second constitutive feature of practical reason is sociality. When
Aristotle asserted that “Man is by nature a political animal,” he did
not mean the facile point that human beings prefer to reside in groups.
He meant that human beings are born into families and families
“naturally” join into groups to form societies. Contra Locke and Hobbes,
living in a society is the “state of nature.” I would suggest that we
can interpret Aristotle’s assertion as a generic. ‘The human being’ is
formally constituted by being an animal that exists not only in a family
setting but in a political setting. Just as ‘the human being’ is a
creature produced by the sexual union of two other human gametes, so
‘the human being’ is able to speak, and to be enculturated in a
particular natural language in a time in human history and a place on
the globe.

The third feature of practical reason is the ability to engage in
rational practices. All organisms initiate *action* in the most general
sense that they move about and do things. And all higher mammals engage
in complex (and often social) practices, such as communal hunting,
grooming, and building. Humans exhibit unique behaviors. We do not
merely *act* – we act *on reasons*. We are the only creatures that set
goals, on purpose, far in advance of their fulfillment. We are the only
creatures who undertake long, complicated sets of actions in order to
achieve those goals. Micah Lott summarizes the specific point about the
human life form: “Human form is characterized by *practical reason*.
This is the capacity to act in light of an awareness of the ground of
our actions, to recognize and respond to practical
reasons.”[@lott2012moral 415. Original emphasis.] Goal-setting and
recognizing practical reasons are inextricably tied. Practical reasons
include our assessments of what is worthwhile. We also reflect on past
actions and evaluate them to decide whether it is advisable to do the
same thing again or try something else. Practical reasoning includes not
just deliberating about what to do but weighing the apparent reasons for
and against a particular course of action. Hence, as I shall explain
later, it is under the category of ‘rational practice’ that I shall
include everything unique about humans having to do with morality.

The fourth feature is rational creation or innovation. Innovative
creation is intrinsically related, I think, to speech, sociality, and
rational practice. That is, one of the forms practical reasoning takes
is that we *innovate* – we create and design and plan actions, new
behaviors, new games, new languages, new activities, and so on. The
structural features of our grammatical system allows us to create new
propositions from a finite set of words, without which we could not tell
stories or write philosophy papers. Furthermore, living within a social
order, practical primates create living spaces, utensils, farming
implements, and so on. We even create new social orders.

The human differentia of ‘practical rationality’ entails not only
abstract reasoning but speech, sociality, rational practice, and
creation. Such norms are not *only* accessible to us, but would be
accessible to an “alien anthropologist” observing humanity from the
“outside.” The alien anthropologist, if indeed it were rational enough
to develop anthropology, could observe these actions and infer the
existence of the property of rationality.

Objections
----------

We must avoid a misunderstanding about the concept of a ‘nature.’ In the
epigraph above, Chris Toner stated that *human nature is normative.* I
don’t insist on the term ‘nature,’ as some object to it on aesthetic
grounds; we could just as well express the point by saying that
genetically modern homo sapiens sapiens are potentially practical,
rational primates. The important thing is not the term ‘nature’ or
‘human nature’ but the concept of a nature. What do I mean by a nature
or life form?

In the old classificatory schemes, philosophers provided a genus and a
differentia to pick out the unique “nature” of any life form or natural
kind. Not every kind-concept corresponds to a real nature: *the set of
medium sized objects immediately to my left* is not a natural kind, nor
is *the set of people born in Ireland.* The kind-concepts under review
are not just any generalizations but scientific and biological kinds
that arise from inquiry and on which inquiry depends. We start out
knowing nothing about an organism (say, some species of beetle) and come
to discover not only that they exist but a whole set of properties:
their genetic traits, their evolutionary history, their natural
habitats, diet, predators, lifespans, and so on. In this way, a nature
is a species, or a homeostatic set of properties, or a natural kind.

When such a kind-concept corresponds to a real natural kind or “nature,”
that nature is potentially discernible both by contrasting it with other
kinds of things and by comparing it with instances of the same kind.
Hans Fink explains:

> The nature of x is both what is special about this x and what makes
> this x one of the x’s as opposed to the y’s. When x is defined per
> genus et differentia both the genus and the differentiating
> characteristic and their combination could be taken to express what is
> the nature of x…. Human nature is what differentiates us from the
> animals and the plants. By nature we are rational beings. Our human
> nature, however, is also that in virtue of which we belong to the
> animal kingdom and to the living organisms. By nature we are mammals.
> We may thus use the concept of nature to differentiate rather than
> include, but also to include rather than differentiate. And we may use
> the concept of nature to express that differentiation and inclusion
> should not be seen as incompatible.[@fink 207]

As Fink points out, the concept of a nature gathers and divides. It
gathers up all the members or putative members of a kind and divides the
kind from other kinds. With this definition in view, we can see what the
point of the old formula was, that man was a rational animal, or a
featherless biped. There are many animals, but few (if any) other
rational ones. There may even be other rational creatures who are not
animals (artificial intelligences, gods, intelligent Alpha Centurions,
or what have you), but so far as we know, we are the only rational
animals in the cosmos.

The best way of reflecting on ourselves as members of the organic
kingdom, as organisms within the evolutionary tree of life, and as
physical objects in the cosmos is to slightly modify the old formula: a
human being is a practical, rational primate. This simple, generic
proposition is astonishingly rich. It captures the facts of our life
form and can be demonstrated to be true from within the human point of
view, and from outside it; an alien anthropologist studying human beings
from its own non-human point of view could discover that humans are
practical, rational primates.

A second misunderstanding has to do with the predication of
‘rationality.’ Humans engage in demonstrative reasoning and practical
reasoning. While both are recognizably modes of *reasoning*, they should
not be conflated with each other.

There is indeed a linguistic parity in the way we talk about π-type
reasons and Q-type reasons.[@edgley1965practical] Both are a species of
“*reasons*,” though they differ in their use. For example, Philippa Foot
says that reasons of type (A) are “Reasons for acting, which we may call
practical reasons” and type (B) are “Reasons for believing, which we may
call evidential or demonstrative reasons.” She continues:

> As philosophers, and therefore theoreticians, our job is of course to
> give the second type of reason, arguing for or against the truth of a
> variety of propositions that seem to involve special problems—like
> those, for instance, about personal identity or the existence of an
> external world. But among these many ‘philosophical’ subjects we find
> that of the nature of practical reasons, and in this special case we
> shall have to give reasons of type B for theses about reasons of type
> A.[@foot2001natural 64-5]

Some unwittingly interpret “rationality” to mean only speculative
reasoning – i.e., mathematical, logical, or otherwise abstract thinking.
This kind of abstract thinking Aristotle would call *theoria* or
contemplative science. I do not think the best way to understand the old
formula of “rational animals” is to take “rational” to mean “abstract
thought” because a nature should capture *all* non-dysfunctional members
of a species and only a relatively small minority of humans engage in
that kind of abstract reflection that characterizes science, theology,
mathematics, metaphysics, ethics, and so on.

Practical reasoning is a better candidate for the single defining
feature because all normal, functioning adult humans, regardless of
cultures, intelligence quotients, or walk of life, engage in practical
reasoning and deliberation. I want to make it indelibly clear that I am
not supposing human nature to be rationality per se but practical
rationality. It is not merely *thought* but *thoughtful action* that I
would like to emphasize. (That practical reasoning is indeed a form of
reasoning, and the difference, if any, between theoretical and
speculative reasoning, is a theme of chapter 5.)

I am *not* saying that only practical reasoning is *active*. Both
theoretical and practical reasoning are active in the sense that both
require intentional effort and both light up the brain on an MRI scan.
The difference between theoretical and practical reasoning is that where
theoretical reasoning results in belief, judgment, speculation, and so
on, practical reasoning *results in action*. And, I would suggest, this
distinction must be built in to our definition of practical reasoning.

That said, the capacity for abstract or “theoretical reason” is
certainly an important feature of human nature and stands out from the
capacities of other organisms. While other members of the animal kingdom
“think” in one sense of that term, as far as we know, no other animal
constructs theories about, say, the cognitive capacities of the animal
kingdom. My only point is to challenge the unwitting interpretation of
“rationality” to mean abstract reasoning to the exclusion of any other
capacity.

A third possible misunderstanding has to do with exceptions to the truth
that human beings are practical rational primates. To quote another quip
from Bertrand Russell: “Man is a rational animal – so at least I have
been told. Throughout a long life I have been looked diligently for
evidence in favour of this statement, but so far I have not had the good
fortune to come across it.”[@russell1992basic, 72] The humor of his
misanthropic jab turns on an ambiguity in the predication of
‘rationality.’ Certainly, many of us are forgetful, neglectful, and
driven by emotion or desire, and our thinking is riddled with fallacies.
If by ‘rational’ we mean the reliability habit of thinking well, then
the possession of rationality would be rare indeed. Children, the
uneducated, the foolish, and many philosophers are not rational by this
high standard. If, however, by ‘rational’ we simply mean the *potential*
to become successfully rational, then every normal human possesses
rationality.

A second misunderstanding, more dangerous than the first, is to think
that someone who cannot successfully think rationally is not even human.
What about anencephalic babies, the genetically defective, the comatose,
the mentally ill – are they not really human? An uncharitable critic
might accuse me of insinuating so. I deny the charge. In fact, one
strength of my argument is that it can explain both why disabilities are
sub-optimal *and* why exactly our disabled fellows are members of our
species. Generics describe a life form well only when the sample
includes exemplary instances of the species – not the young, immature,
ill, injured, genetically defective, radiation poisoned, comatose,
mentally ill, and so on. However, such are still recognizably members of
the species. Humans are “bipedal” by nature even when someone (say, a
war veteran) is no longer bipedal. Anencephalic babies who lack the
subvenient brain structure necessary for rational consciousness are
“rational” by nature even though they will never exemplify their
potential for practical reasoning. Abnormal members of our species are
recognizably *human* – they are not eagles or moon rocks or dandelions.
We have a clean explanation for this, for generic truths are compatible
with individual exceptions. Indeed, without well-grounded knowledge of
the life form expressed in generic propositions, it would be impossible
to describe any individual as abnormal, immature, ill or injured.

A final possible misunderstanding needs a response here. Someone might
observe that terms such as “exemplary” or “normal” or “mature” are
normative terms and hence charge that I am “smuggling” evaluations in to
a process of objective, scientific description. I welcome the
observation, but deny the charge. The discernment between ordinary,
unusual (but not defective), and abnormal (and defective) is certainly
an evaluative discernment. My point has been that such evaluative
discernment is part and parcel of objective, scientific generic
predication. Researchers do not judge the characteristics of a newly
discovered species of beetle by examining its young. They might, at
first, mistake the initial specimen for a fully mature adult; but the
correction would come from a further application of scientific methods.
The capture of a larger beetle that appears to be *of the same kind*
would suggest that the initial specimen was either a child or a runt.
After collecting a sufficient sample of specimens (say, a dozen or
preferably more) the researchers would be in the position to make
justifiable fundamentally normative judgments about *which of these
individual beetles is exemplary of the species.*

We can draw the same conclusion with a hypothetical situation in which
humans are the newly discovered species. Suppose an alien anthropologist
were to stumble across earth and study humans. Suppose that the initial
specimen was a 12-year-old boy or girl. If that was the anthropologist’s
*only* sample, the alien race would come to all sorts of incorrect
conclusions about humanity in general. If, instead, they studied mature,
healthy, human beings of both sexes, in the “prime” of life, they would
be closer to identifying what is generically *human*. My contention is
that they would be best served not by examining foolish humans but
practically wise ones.

I conclude that the ascription of practical reason to human beings is
indeed true generically of the human life form, species, or nature. The
rarity of successful realization of a capacity for practical reasoning
does not tell against the truth of the generic, and neither does the
existence of persons who may never actualize the capacity. Such
exceptions rather support the thesis, for how else could we judge that
there is a *genetic defect* except by reference to the genetic norm?

### No Organic Natures

There are a few other objections a reader might have at this juncture.
The first objection is simply that we cannot identify “human nature”
with any scientific accuracy because there is no human nature. This
objection has three iterations.

The first sort of critic might deny that there is any such thing as a
human life form because there are no life forms at all. This is an
objection to the very concept of a nature. Perhaps, instead of real life
forms and natural kinds, we should be nominalists about divisions
between various branches of the tree of life.

One iteration of this criticism is an alleged tension between the
flexibility of species (as represented in evolutionary biology) and a
fixed notion of human nature. In a seminal paper on natural teleology,
Ernst Mayr says:

> The concepts of unchanging essences and of complete discontinuities
> between every *eidos* (type) and all others make genuine evolutionary
> thinking impossible. I agree with those who claim that the
> essentialist philosophies of Aristotle and Plato are incompatible with
> evolutionary thinking.[@mayr1970populations 4]

Arthur Ward is a recent critic who agrees with Mayr on this point. Ward
argues that “naturalists should reject the idea of ‘human nature,’ and
indeed should reject that any organism or its parts or operations has a
nature, purpose, proper function, or the like.”[@ward2013against 1] I
have already pointed out that rejecting all organic natures and purposes
is not necessarily the only rational, scientific option; indeed, such a
rejection seems to me to be motivated by philosophical materialism far
more than it is motivated by any respect for actual biological science.

The arguments of the previous chapter, built on the assumption of a
minimal scientific realism, is enough to secure a fairly solid grounding
for the notion of natural kinds. Nevertheless, I cannot insist that
accepting organic natures and purposes is the *only* rational,
scientific option. Nor can I chase down the (justifiably important)
dispute about the status of natural kinds. I only ask the reader to
consider that both views are live scientific options.

### No Natural Teleology

A second sort of critic accepts natural kinds but denies that these
kinds have teleological features. For example, Bernard Williams asserts
that: “The first and hardest lesson of Darwinism, that there is no such
teleology at all, and that there is no orchestral score provided from
anywhere according to which human beings have a special part to play,
still has to find its way into ethical thought.”[@williams2011ethics 44]
Williams says elsewhere:

> The idea of a naturalistic ethics was born of a deeply teleological
> outlook, and its best expression, in many ways, is still to be found
> in Aristotle’s philosophy, a philosophy according to which there is
> inherent in each natural kind of thing an appropriate way for things
> of that kind to behave.[Cf. @williams1995making 109]

This sort of critic thinks that there are natural kinds and stable
species with objective properties, but does not accept the notion that
functional or teleological properties feature in purely biological
descriptions of organisms.

Williams voices a common opinion when he alleges an incompatibility
between Darwinism and teleological realism. The proper response, as
articulated by Hursthouse, Foot, Brown, etc., is that natural teleology
is indeed compatible with Darwinism and does indeed provide “an
appropriate way to behave” (or we might add, *ways*) that is “inherent
in each natural kind of thing.” Natural teleology is not incompatible
with evolutionary theory.

Strictly speaking, evolutionary theory is a set of theses explaining the
current multiplicity and shape of terrestrial life. It says absolutely
nothing about teleological causes or properties.[^35] There is room, in
other words, within evolutionary theory for discussions about the
evidence for or against non-mechanical teleological causation. Thomas
Nagel is one who recently presented such a naturalistic theory of
Darwinian natural selection combined with teleological
causation.[@nagel2012mind . Briefly, he suggests that while physical
laws work impersonally on entities at a given time, teleological laws
might work impersonally on the same entities over time.] I do not wish
here to defend Nagel’s view so much as to point out that teleological
realism is compatible with evolutionary theory. Merely *asserting* that
teleological realism in biology is incompatible with Darwinism does not
make it so. Naturalistic teleological realism is certainly incompatible
with a teleological nihilism distinctive of (certain brands) of
metaphysical reductionism. If our knowledge of natural teleology is
well-grounded enough then so much the worse for metaphysical
reductionism.

One other response to Williams is possible. Williams despairs of finding
human nature, including a human telos, because he thinks that modern
biological science somehow demands such despair. Rosalind Hursthouse
correctly points out that Williams’ worry is not actually rooted in the
progress of modern science. Williams himself admits that “many of course
have come to that conclusion before… that human beings are to some
degree a mess… for whom no form of life is likely to prove entirely
satisfactory, either individually or socially.”[@hursthouse1998virtue
261, quoting from Williams.] If many have come to that (philosophical)
conclusion before, without the benefit of modern science, why would we
think modern science is definitive for this philosophical conclusion? If
modern science provides additional warrant for rational despair that was
unavailable to our ancestors, what exactly is that evidence? It is not
enough to gesture. According to Hursthouse, Williams’ worry is not an
argument at all but an expression of moral nihilism. He despairs of
finding one purely satisfactory way of life, and so concludes that human
beings are a mess. His may be a rational despair. But citing biological
facts cannot prove it so. Whether we should despair or not must be
settled by philosophical argument. To amass scientific evidence for p
and then to assert the philosophical conclusion that q is a non
sequitur.

### Only Biological Nature

A third iteration of the “no human nature” objection is that if there is
such thing as “human nature” it is nothing more or less than our
biological and physiological makeup. Tim Lewens argues that “the only
biologically respectable notion of human nature that remains is an
extremely permissive one that names the reliable dispositions of the
human species as a whole. This conception offers no ethical
guidance…”[@lewens2012human] On Lewens’ view, the only talk about our
“nature” that would be scientific would be an indeterminate series of
complicated stories about physical status and history: our genetics,
evolutionary history, neurophysiology, geography, and sociobiology. As
Arthur Ward says, “one can affirm that humans have many innate instincts
explained by evolutionary processes, yet deny that humans have a
“nature” strictly speaking.”[@ward2013against 1] The problem, as we have
seen, is that an empirical “scientific” conception of human nature has
nothing to do with *ethics*. All of the complicated stories we could
tell – if they are genuinely scientific – would be purely
*descriptive*.[^36] Bernard Williams expresses a similar objection by
saying that nature has bestowed upon us an “ill-sorted bricolage of
powers and instincts.” He continues:

> [the problem] lies not in the particular ways in which human beings
> may have evolved, but simply in the fact that they have evolved, and
> by natural selection… On that [evolutionary] view it must be the
> deepest desire – need? – purpose? – satisfaction? – of human beings to
> live in the way that is in this objective sense appropriate to them
> (the fact that modern words break up into these alternatives expresses
> the modern break-up of Aristotle’s view).

Williams objects that norms bestowed by the process of evolution would
be those that lead us to survive and reproduce. Along similar lines,
Fitzpatrick articulates a worry that evolution has bestowed upon us a
very specific, ordered power but it is not the power to flourish but the
power to reproduce. He says:

> If, however, natural functions and ends in living things are
> structured by special relations established through the process of
> evolution through natural selection, i.e., non-incidental relations
> between traits and a special subset of their effects that figured into
> the selection process, then natural teleology will not ultimately or
> generally be about the welfare or flourishing of
> organisms.[@sepmoralitybiology . Cf. @fitzpatrick2000teleology]

On Fitzpatrick’s worry, the fact that there might exist natural human
norms to reproduce is irrelevant to whether or not willfully conforming
to such norms would contribute to our welfare.

A third proponent of this worry is Stephen R. Brown. Brown’s defense of
virtue ethics is ambivalent. He seems to *wish* he could make the
account genuinely normative but concedes that it is, in the end, merely
descriptive.[@brown2008virtue] Even virtue ethics, after being
appropriately “naturalized,” does not *commend* the virtues so much as
*detail* the traits which happen to be adaptive for creatures like us to
survive and propagate our genotype.[@brown2005really] Brown thinks that
human beings do have a characteristic form of life involving highly
rarefied neurological and cognitive processes we do not observe in other
animals; but, nevertheless, he thinks that biology reveals that species
are the only natural kinds, and species aim to survive and reproduce.

### Responses

The objection that human nature is *merely* a biological (and hence
descriptive) concept is a relevant one. Despite the varying details,
what Lewens, Fitzpatrick, and Brown agree upon is that if such a thing
as human nature or the human life form exists, and if such a thing as a
natural teleological norm for humanity exists, then it is the norm to
reproduce and propagate one’s genotype. Three comments are required to
untangle this objection.

First, even granting that reproduction is the only natural end of
non-human organisms, Lewens et al. assume that human beings are *merely*
animals. This can be queried. Above, I asked the innocuous question: Are
human beings natural organisms? There are really three slightly
different answers: the non-naturalist answer is that humans are natural
plus something more than natural;[^37] the reductive naturalist answer
is that human beings are natural organisms like chimpanzees and nothing
more; the non-reductive naturalist answer is that human beings are
natural organisms, leaving the rest to one side.

My view is that humans are *at least* natural organisms. Hence, my view
can accommodate both non-reductive naturalism and non-naturalism. The
only position *incompatible* with mine is the crassly reductive one that
asserts that human beings are no different from other primates – even in
being practically rational. I can agree that human beings as a species
are endowed by their history with a natural norm that leads them, absent
countervailing factors, to reproduce. I simply deny that *that is all*.
The only way these authors can sneak in the view that *that is all* is
by begging the question in favor of a reductive view of humanity.

The reductive naturalist would insist that “human beings are natural,”
meaning that humans are merely machines made of meat, “heaps of
glorified clockwork.”[@pinker2003blank] Smuggled into this assertion is
the assumption that nature is bald. Humans are one of its myriad
variegated objects and just parts of the heap. I have tried to argue
above that even bacteria and plants give the lie to this picture.
Furthermore, the irony is that if human beings were *merely* animals,
and subject to *merely animal* natural norms such as instinctual
survival and reproduction, we could not *know* ourselves as such. Yet
the objection Lewens et al. are posing depends on knowing ourselves as
both animals and as self-aware practical reasoners.

My view, by contrast, is based on the empirical observations that humans
are the only primate to engage in recursive, grammatical speaking; to
associate in such complex societies; to plan their actions; and to
innovate and create. Those observations are enough to render it plain, I
think, that our natural telos is not restricted to only to that which we
share with the rest of the living world but must include our peculiar
capacities for rational reflection – including rational reflection about
whether or not to reproduce.

Secondly, Lewens et al. assume that the only natural end of organismic
life is reproduction. But this can be queried as well. Certainly, living
things sustain their own health and life and animals propagate their
genes; living things *sustain* their life form and *transmit* their life
form. But which is for the sake of which? Do organisms live in order to
reproduce or reproduce in order to live? I do not see how one can assume
this to be true without further argumentation. Empirically, we observe
*both* that each species propagates its genotype *and* that each species
lives its own particular form of life aiming at the development of its
own good. My view is that reproduction is *one* of the natural ends of
organic life, but that each species has other natural goods, such as
health, survival, and the living of a characteristic life. Reproduction
is a minimal good without which the other goods could never come to be.
However, these other goods may or may not have anything to do with
reproductive success. Above, I defended two kinds of natural
normativity: the mere existence of creatures bearing life forms as well
as their teleological development into fully matured instantiations
thereof. An embryonic mammal *is to become* a fully grown mammal. Hence,
a human is a practical primate and a practical primate *is to become* a
fully mature practical primate. In other words, one of the “norms” of
practical rationality, we can venture, is that we *ought to be
successfully practically rational*. Practical rational activity and
success is part of what it means to be a healthy human being living our
characteristic sort of life.

Thirdly, I would try to accommodate the insights of Lewens et al. by
conceding that reproduction is *one* of our natural ends. However, we
need not jump to the conclusion that it is the *only* natural end or the
only fundamental natural end. “Human beings reproduce” is an instance of
a broader natural generic truth we can articulate by saying: “organisms
survive and reproduce.” Human reproduction as a generic pattern is
compatible with exceptions: The celibate, the pre-pubescent, the single,
the infertile couple, the homosexual couple, and others do not reproduce
directly and without aid. Nevertheless it may be true that humans
reproduce (like every other organism). That *any particular individual*
does not reproduce is not an automatic sign of defect. It seems to me
that if, *as a species*, we ceased to reproduce, something would have
gone wrong.[^38]

Making the distinction between the individual member of the species and
the species itself raises other potential problems: Is the human norm to
become virtuous merely species-specific and not specific to the
individual? (I shall address this problem more fully in chapter 4.) For
now, I must be content to assert that some virtues are required for the
flourishing of both species and individuals, while practical wisdom is
required for *every* individual member of the species since that is what
we are.

### Knowing from Inside or Not Knowing At All

There is one further objection that I will return to in chapter 5, but
that deserves a mention here. The objection that human nature is
*merely* animal and hence the human telos is *merely* survival and
propagation of the genotype was supposed to tell against the organic
teleology I have been defending. My response is that, in practical
rational creatures like us, our biological norms are joined with other
norms.

In one sense, these critics agree with me. They think it is “obvious”
that reproduction is not our *only* norm and so the merely “natural” or
“biological” norm must be supplemented with the practical point of view
– the point of view from within human subjectivity. Their worry is that
once we introduce the practical point of view we are leaving biological
naturalism behind. This is sometimes called “the Irrelevance Objection.”
I offer a fuller response to the Irrelevance Objection in chapter 6.

A final objection might come from someone who simply urged that human
nature is mysterious. For all we can tell without the benefit of divine
revelation, humanity is an anomaly. Our origin is shrouded in mystery,
our destiny undecided. \newline
\indent I concede the point. My thesis is not that we already know
everything about humanity that we ever will know or need to know. My
thesis is that observing our nature as practical primates is a minimal
starting point of knowledge upon which to build. Knowing that snakes are
legless reptiles is not an end to scientific inquiry about them, but a
beginning. Indeed, one cannot begin to learn more about ‘snakes’ unless
one apprehends that ‘snakes’ exist and roughly what they are. So
capturing the genus and differentia of a kind of organism is in fact
necessary for creating a conceptual placeholder *on which to attach new
knowledge*. Knowing what human beings are, however roughly, gives us a
concept-category within which to fill in the depth and breadth of facts
and information. \newline
\indent The main thesis of this chapter has been that the following
generic is true: “human beings are practical, rational primates.” This
generic, I have argued, is defensible both philosophically and
scientifically. It is discoverable both by humans examining our species
from “within” the human point of view and by alien anthropologists
examining our species from “outside” the human point of view (so long as
they too were intelligent and rational). This generic picks out a
property or set of properties we might describe as *human nature*. If
this is anywhere near to correct, then human nature is not a complete
mystery. We know *enough* about it to build a neo-Aristotelian theory of
ethics grounded in evaluations of human beings by reference to the human
life form.

Natural Norms, Human Norms
--------------------------

If the argument has been successful thus far, then, the best evidence
suggests that human beings are practical, rational primates. This
generic captures a set of truths about the human life form and natural
telos in the same manner as other respectable scientific statements,
such as ‘the platypus is an egg-laying mammal’ and ‘the baby chick
becomes a rooster.’ What is the ethical significance of this
proposition? The remainder of the chapter fills out some details of the
picture.

As natural organisms, humans pursue certain basic goods: food, water,
rest, shelter, comfort, survival, reproduction. There is every reason to
affirm the truth of generics such as “human beings eat food” or “human
beings sleep daily.” We should hypothesize that deviation from these
prima facie norms would be prima facie defective. And that turns out to
be the case. Anorexia, starvation, insomnia, and so on are disorders.
Importantly, such disorders would plausibly be recognizable by an alien
anthropologist. Just as a scientist may evaluate a particular wolf by
reference to its life form, an alien anthropologist could evaluate a
particular human’s life and actions by reference to its life form. So
much applies to both humans and other organisms.

Things get really interesting – and much more tricky – when we consider
humans as reasoners. I have used the term ‘practical primate’ to
encompass all the ways in which human beings distinguish themselves by
being scientists, moral agents, planners, creative writers,
deliberators, speakers, political agents, and so on. As mammals, human
beings pursue mammalian goods. As practical rational agents, human
beings also pursue practical rational goods: wisdom, friendship, world
travel, education, entertainment. These seem categorically different.
Are they so different as to ruin the pattern of naturalistic evaluation?
Michael Thompson thinks not:

> … will and practical reason are on the face of it just two more
> faculties or powers a living being may bear, on a level with the
> powers of sight and hearing and memory. The second crucial thought is
> that an individual instance of any of the latter powers – sight,
> hearing, memory – is intuitively to be judged as defective or sound,
> good or bad, well-working or ill-working, by reference to its bearer’s
> life-form or kind or species.[@thompson2008life 29]

Naturalistic evaluation of human beings on the basis of practical
rational activities follows the same pattern as before. Every animal’s
nature or life form has genus and differentia. For human beings, our
differentia is that we can engage in practical reasoning. Hence, our
animality and our rationality both count. Being a primate entails that
we are alive and share properties in common with all organic nature.
Being a practical reasoning primate includes a set of capacities,
including abstract thought but also more: speech, sociality, rational
practice, and creativity. I also argued that the generic truth about
humanity holds good in the face of important objections to the effect
that we have no nature, or that our only nature is biological.

Some might object that the thesis, as it stands, is vague: do natural
norms bind all individuals or only some? Does practical rationality free
us from natural norms in certain cases? Thus far, I have argued that
there is good reason to affirm a kind of prima facie natural normativity
binding on anyone who belongs to our human species. I concede that I
have not yet fully articulated what effect rationality has on our animal
nature and rebutted the objection that it renders irrelevant all the
prima facie natural norms arising from our animal or biological nature.
Rendering this more clear is a task for the next two chapters on virtue
and practical reasoning.

Here, I shall only point out that even the objection cites our ability
to practically reason about our life form and its attendant natural
norms, which reinforces the thought that humans are obligated to
practically reason *well*. The new natural criteria by which to judge
the human organism include reference to the practical rationality of its
life form. For example, consider generics such as these: “The human
being acts upon reflection”; “the human being speaks a language”; “the
human being lives in society,” and so on. These natural human norms are
well on the way to being genuinely ethical. Deviations from them
represent genuinely *human* defects. Folk morality recognizes something
wrong with the jolly fool who willfully acts before deliberating, or the
blowhard who willfully speaks without restraint, or a paranoid hermit
who willfully avoids all human society. Naturalistic evaluation explains
*what exactly* is wrong. Such persons are not living up to their own
human life form.

A couple of clarifications are in order: First, I am by no means
suggesting that physical disability or psychological illness constitute
“moral defect.” Even serious mental illnesses can be borne by the
virtuous and mature adult. Rather, the defects that do inhibit living a
fully human life are defects of practical reasoning. Someone
hearing-disabled or born without arms might be inhibited from
widely-enjoyed pleasures of hearing music, say, or playing certain
sports, not inhibited from achieving their deeper natural ends. The same
can be said for mental illnesses such as depression and anxiety. A
person with chronic depression, say, faces pressing challenges in every
day life that are liable to inhibit certain pleasures. Nevertheless, in
striving to cope with the local illness, it is possible that the extra
effort of facing daily challenges can result in a more rapid acquisition
of certain virtues, such as patience and courage.

A second clarification is this: Even if I am successful in articulating
certain generic truths about humanity, not all the details have been
supplied. I aim to capture the foundations of morality, not every last
detail. Hence, my account will be a step toward providing a rational
basis for evaluation of the vast majority of individual human beings,
but it is possible (and indeed quite likely) that I have not touched on
certain extreme outliers. For example, persons of extreme practical
wisdom are able to determine, correctly, when acting contrary to
received social norms, or speaking without restraint, or living in
solitude are the thing to do. Larissa MacFarquhar details cases wherein
donors offer kidneys to strangers and foster parents adopt dozens of
children.[@macfarquhar2015strangers]

Likewise, persons of extreme practical folly are able to convince
themselves that the “rules do not apply” to them. In some cases, extreme
folly can be terrifying, as when it is joined with a mad quest for
political power and personal gain, as Hitler or bin Ladin who had *some*
conventional virtues and plenty of intellectual competence to put toward
their heinous ends. In other cases, extreme folly can be pathetic, as
when it is joined with self-defeating helplessness and spite.
Dostoevsky’s Underground Man demonstrates such extreme folly:

> I am a sick man…. I am a spiteful man. I am an unattractive man. I
> believe my liver is diseased. However, I know nothing at all about my
> disease, and do not know for certain what ails me. I don’t consult a
> doctor for it, and never have, though I have a respect for medicine
> and doctors. Besides, I am extremely superstitious, sufficiently so to
> respect medicine, anyway (I am well-educated enough not to be
> superstitious, but I am superstitious). No, I refuse to consult a
> doctor from spite. That you probably will not understand. Well, I
> understand it, though. Of course, I can’t explain who it is precisely
> that I am mortifying in this case by my spite: I am perfectly well
> aware that I cannot “pay out” the doctors by not consulting them; I
> know better than anyone that by all this I am only injuring myself and
> no one else. But still, if I don’t consult a doctor it is from spite.
> My liver is bad, well–let it get worse!

While admitting that he is sick, he lets it get worse. While admitting
that doctors know what to do, he doesn’t consult them. While admitting
he should not be superstitious, he is. While admitting that he is
hurting himself, he continues out of spite. Dostoevsky’s character is
fictional but anyone who has come across such a dizzying person in real
life is aware that the normal methods of encouragement and persuasion
are ineffective. Thus far, my thesis has not offered an explanation of
such extreme outliers. Nevertheless, articulating what is true of
humanity *generically* provides a foundation from which it is possible
to assess the outliers. What makes the Underground Man so pathetic as a
type (and so powerful as a literary character) is that he seems
*inhumanly* wretched. My account offers a plausible explanation: he
falls short even of enjoying a basic, human level of practical wisdom.

We are now in the position to articulate a second ethical upshot of the
generic that human beings are practical, rational primates. If acorns
are (potential) oak trees, then it seems to follow that an acorn *is to
become* an oak tree. I won’t insist on using the word ‘ought’ (the acorn
*ought to* become an oak) because ‘ought’ talk strongly suggests agency
and it would be silly to ascribe agency to lower organisms. But I do
insist on the *natural normativity* of that statement. The individual
acorn that fails to become an oak *never* fully realized its nature.
Likewise, if human beings are practical rational primates, then it
follows that human beings *are to become practical rational primates*.
This normative generic proposition is rooted in the thought that humans
*are* practical rational primates. But it goes further to suggest a
teleological end: we are to become (in full actuality) what we already
are (by virtue of membership in our species).

Becoming fully mature or fully actualized practical rational primates
requires the actualization not only of our animal nature (through
growth, maturity, reproduction) but our rational potential through
intellectual growth and knowledge, and practical wisdom that sublimates
all of one’s emotions and bodily desires and physical settings into a
good life. In other words: Humans *are to become* practical, rational
animals.

I do not intend to suggest that there is something inherently morally
praiseworthy about the acquisition of factual knowledge, understood in
terms of institutional education or advanced degrees. There is nothing
inherently morally defective about a person or culture who lives in, for
example, in ignorance of advanced knowledge about biology, chemistry,
astronomy, and mathematics. Rather, every person from every walk of life
at every stage of life stands in need of *practical wisdom.* One of the
recursive aims of practical reasoning is to determine just how far and
in what areas one needs to advance one’s knowledge: a lawyer who does
not spend years studying case history would be just as unwise as a
farmer who does do so. Both would benefit from reflection on more
universal human tasks such as making and maintaining friendships,
dispatching familial and social commitments, and so on.

If our nature is to be practical, rational primates, then we have some
general notion of our natural “function.” I shall not go in for the
Aristotelian view that the natural work (Greek: *ergon*) of human beings
is contemplative science, an activity by reference to which success and
failure may be judged. Rather, I shall be more ecumenical: the telos of
every life form is, at the very least, to do all the activities that
constitute its mature flourishing. So we should predict quite generally
that the human telos is to become *fully mature* practical, rational
primates. The conceptions of human nature (as practical reasoning
animals) must be defined in relation to virtue (the excellences of
rational practice and practical reason) and to human nature as it could
be, our natural telos (to be excellent and mature practical, rational
primates).

The third ethical upshot has to do with excellence. Suppose that the
excellence of species x is a quality that both constitutes being an x
and enables an individual to realize x-hood. Having a bill or being able
to swim is both constitutive of being a penguin and also enables the
young penguin to develop into maturity and realize its nature. Now apply
that same pattern of evaluation to a human being. What are the
excellences that are both intrinsic goods-of-a-kind for creatures like
us and also instrumental to realizing our natural telos? The answer is:
the virtues.

Virtues enable one to be a practical, rational primate, but they are
more than instrumentally valuable. Virtues on my account will turn out
to be *constitutive* of humanity in the sense that having them is both a
path to realizing one’s life form and also part of the definition of
expressing that life form. It may seem to odd to categorize essential
properties of humanity as morally praiseworthy traits. But the point is
essential to my case. Virtues are not just “morally praiseworthy”
qualities; they are *the human* qualities. Virtues are examples of
*humanness* in its exemplary form.

I grant the notion that virtues are “the human” qualities is a reversal
on the all-too-common notion that “human” qualities are neutral with
respect to moral praise or blame. The common notion is a mistake, so the
reversal is justified. As I tried to argue above, all life forms
discovered by scientific investigation and articulated in generic
propositions are inherently normative. Hence, the concept of human
nature cannot and should not be value-neutral. Rather, as Micah Lott
points out, the concept of human nature:

> …must embody a normatively significant understanding of human life and
> action. For any conception of human form is a natural-historical
> account of ‘how the human lives.’ As with ‘the tiger’ or ‘the mayfly,’
> a natural-history of ‘the human’ provides an interpretation of the
> characteristic and non-defective life-cycle of the
> species.[@lott2012moral 770-1]

Virtues on my account will turn out to be qualities that enable one to
become – and partly constitute one’s being – a mature organism. As I
shall detail more in chapter 4, virtues are not just *any* natural good,
for our physiological life consists of a process of maturation,
nutrition, rest, exercise, homeostatic maturity, reproduction,
characteristic activities, aging, and death. Many human goods enable
this process, from oxygen, food, sleep, and so on. However, the virtues
are a subset of natural goods pertaining to one’s actualization of
excellent practical reasoning and excellent rational practices. The
virtues enable one to perform characteristically rational activities
such as speaking, socializing, thoughtful acting, and creating. As I
argued above, the peculiarity of our life form is that we are inherently
self-aware language-users who grow up and live in a language-community
with a history and tradition, and who are curious to know what is true
about ourselves and our world. We are also extravagantly innovative,
creating a myriad of tools, forms of art, and other products for our use
and enjoyment. We are inherently conscious and self-conscious beings who
speak, interpret, and create in the context of a linguistic community
such as a family, society, and culture. We are inherently goal-oriented
and self-determining beings who are to some degree able to acquire new
traits or lose them, able to achieve our natural ends or fail to achieve
them, able to become aware of the “givenness” of our biology and work
with or against it, and are able to treat an entire biological life not
only as an event but as a project. Although we are pushed about by our
biological instincts and by social pressures, we do not *simply* stumble
around through life; at times we also act on *reasons*. That is, we
deliberate about future actions, and reflect on past actions, and become
puzzled in the present about what is called for. The success of our
actions is not guaranteed, and the reasonableness of our justifications
is not guaranteed. Rather, we muddle through on the best evidence we
have.

The criterion of a definition of virtue, then, is that the excellences
intrinsic to our life form are those traits that practical rational
primates per se *need* to be what they are and to live life in such a
way as to become what they can potentially be. Prima facie, a basic set
of virtuous traits such as courage, moderation, and practical wisdom are
incumbent upon every member of the species. There is room, even so, for
further reflection and specification of virtues needed – more here, less
there – by individuals belonging to varying life circumstances, social
roles, and differing stages of life. I shall attempt to provide a bit
more specification in the following chapters.

Just as important as specifying the basic set of virtues that constitute
natural goodness is identifying the basic set of vices that constitute
natural defects. *Natural badness* would include all those traits that
practical rational primates as such *need to avoid*. Vices would be
those acquirable traits over which one has some measure of control,
rather than just any natural evil such as hunger, exposure to predators
or extreme temperatures, disease, accidental injury, and premature
death. Non-moral natural evils such as these do indeed tend to frustrate
one’s development toward the natural end of being a fully mature
practical reasoner and hence each one partly constitutes
species-specific misery. We should expect that moral vices (such as
cruelty) at least partially contribute to other natural evils (such as
premature death). But we ought not confuse the two. Even a virtue such
as commendable generosity with one’s resources might lead to hunger, and
commendable courage might lead one to premature death. However, the
acquisition of a vice is the voluntary infliction of a natural, moral
evil upon oneself and, potential, on others as well.\newline

\indent One final objection deserves mentioning. The cool-headed despair
of a J.P. Sartre would deny that human nature exists, ready-made, prior
to one’s willful self-creation and self-expression. He would deny,
therefore, my picture of natural goodness as the excellent performance
of one’s function understood as the actualization of one’s intrinsic
life form. Instead, he would insist that we are radically free to choose
what we are and what we will become. The shape of this Sartrian thesis
certainly sounds quite different from mine – but is it so different?
Sartre agrees with me that what one *is* determines what one *ought to
be*. For he says: “my freedom is perpetually in question in my being; it
is not a quality added on or a property of my nature. It is very exactly
the stuff of my being.”[@sartre 566] He agrees with me that one cannot
choose to *not* choose. One is *necessarily* free. While one must decide
*what else* is true of one’s nature, one cannot choose to be an unfree
thing. While Sartre’s existentialist picture of a human being is that it
is simply freedom, a pure will, a choosing thing, my more scientific
picture is that a human being is a practical, rational primate. Our
nature is constituted by both the genetic, biological, and physiological
as well as the psychological and practically rational. Hence, on my
view, the set of actions one must *necessarily* do is larger than simply
the action of choosing. For example, one must become practically wise
because one is practically rational. Just as Sartre would accuse someone
who tried *not* to choose anything of bucking their nature, I would
accuse someone who tried *not* to be a practical reasoning animal of
bucking their nature. We agree that rebelling against one’s own nature
and life form is futile and foolish; we disagree about how best to
characterize that nature and life form.

Conclusion
----------

This chapter has argued that human beings are practical, rational
animals. I addressed and responded to several objections, and tried to
bridge the connection between the descriptive/normative generic that
sets the standard for our life form, and also show how specific ethical
obligations fall out of that normative foundation: there is a prima
facie obligation to eat or sleep and keep oneself alive, or to become
fully practically rational over time. And I began to sketch how the
specific qualities of excellence for practical rational primates are
moral and intellectual virtues, including moderation and immoderation,
justice and injustice, practical wisdom and foolishness, and so on.

The hypothesis is that virtues are a specific type of quality belonging
to creatures like us. Virtues are the human specific goods-of-a-kind.
The virtues constitute a set of normative constraints on what one is and
what one ought to become arising from one’s nature as a practical
primate. The acquisition, then, of virtues both causes and constitutes
the actualization of our life form as practical rational primates. Truly
exemplifying our life form constitutes our species-specific flourishing.
Virtues are commonly supposed to be “excellences” of human beings.
Relative to what is such a quality excellent? The answer can only be
that virtues are excellences relative to our nature or life form. They
are the traits or qualities that enable us to actualize our life form,
to fully express in a life what we are by nature. If what we are by
nature is practical, rational primates, then virtues (we can further
predict) will be traits pertaining to practical reason and animality.
The sketch of a fully virtuous and wise human being would not, on this
account, describe an unattainable moral ideal; like a painting of a
fully grown oak tree, it would describe the natural state of a human
being that has arrived at its natural end. It would be a sketch of what
we truly are.

What We Are
===========

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{Human nature is normative, such that to be morally good is to fulfill one’s nature.}%
 {---\textsc{Christopher Toner, \lq\lq Sorts of Naturalism,\rq\rq 221.}}
 \centering
 \end{epigraphs}
The previous chapter laid out the criteria a naturalistic account of
virtue would have to satisfy. Just as excellent specimens of any natural
organism reflect an inherent natural normativity, excellent human beings
would reflect an inherent “human” normativity that arises from our
nature as practical, rational primates. Human norms must be *animal*
since we are primates; they cannot be *merely* animal since we are
*practical* primates with a peculiar form of life.

My thesis in this chapter is a normative one: virtues for practical
rational primates are excellent rational practices and practical
reasoning – while irrational practices and practical irrationality are
natural vices. To put a fine point on it, the description of a fully
virtuous agent is a more accurate description of ‘the human being’ than
any mere statistical generalization. Human virtue – and especially
practical wisdom – describe *what we are*. The task of the moral life is
to become what we are.

My purpose is to defend this paradoxical notion by building on the
normative virtue theories of Foot, McDowell, and MacIntyre.[^39] These
neo-Aristotelians show how it is possible to evaluate the kind of life
one is actually living with reference to the normatively human. I also
discuss and critique their accounts. The result is a unified view
according to which virtues are excellences of rational practice and
practical reasoning, while vices are constituted by irrational practices
and defective practical reasoning.

Section 1 draws from Foot, McDowell, and MacIntyre to develop a concept
of virtue: firstly, virtues benefit humankind (including but not limited
to their possessor) while vices harm. This point breaks down the
putative divide between altruistic or other-regarding and self-regarding
virtues.

Section 2 argues that virtues constitute excellent human *functioning*
and that they are especially beneficial in that they are corrective of
tempting vices. Section 3 virtues are not just any positive traits such
as those given by luck, nor are they necessarily even *acquired* at all
– rather, virtues are in principle *acquirable*. Section 4 argues that
some virtues are excellences of “rational practicing” while others are
excellences of practical reasoning about one’s whole life. Section 5
argues that virtues are excellences of “social reasoning” in that they
enable the health and progress of societies and traditions.

Virtue as Natural Goodness
--------------------------

Foot, MacIntyre, and McDowell each offer detailed accounts of virtue and
its relation to reason and nature. For example, Philippa Foot argues
that virtues are the acquirable, beneficial, corrective excellences of
practical reason.[^40] Alasdair MacIntyre argues that virtues are
“acquired human qualities” that enable the virtuous person to succeed in
individual practices, in life, and in traditions.[@macintyre1984after
191] John McDowell argues that virtue is a kind of perceptual
sensitivity to what is required to live well.[@mcdowell1979virtue 331]
My goal in this section is to articulate a fairly comprehensive
treatment of virtue, drawn from what these three writers agree on, but
sensitive to what they disagree on. I shall first state eight points
about virtue and vices that bring these ethical concepts into clear
light.

The first point about virtue is that virtues are beneficial to their
possessor. Hursthouse calls this “Plato’s requirement” on the virtues:
“The concept of a virtue is the concept of something that makes its
possessor good: a virtuous person is a morally good, excellent or
admirable person who acts and feels well, rightly, as she should. These
are commonly accepted truisms.”[@sepvirtue] While virtues may come with
a cost, there is something counterintuitive about the notion that X is a
virtue that could, in the end, ultimately be a detriment its possessor.

As we have seen, this requirement fits Foot’s account of natural
normativity. As some traits make a ‘good oak’ or a ‘good wolf,’ a good
person exemplifies those good-making traits shared by all exemplary
members of a natural species. Virtues are good-of-a-kind for creatures
like us, namely, practical rational primates.

MacIntyre agrees. For MacIntyre, virtues are “acquired *human*
qualities.”[^41] Such human qualities enable their possessor to achieve
particular *goods.* MacIntyre’s second clause assumes that virtues are
beneficial. For MacIntyre, a virtuous trait *cannot* be directed at
achieving what is bad.

Assuming that virtues cannot go bad will bring some trouble for
MacIntyre’s initial definition in *After Virtue*. It seems quite
possible that people who have particular virtues can be, overall,
wicked. Can’t the thief be courageous, the dictator magnanimous, the
glutton affable, the prude moderate? MacIntyre indexes virtues to the
*goods* internal to practices, but can’t practices themselves be wicked?
We might say this is the problem of *virtue going bad.*

I should explore three possible responses to this problem before
offering my own solution. The first response is to stipulate away the
possibility that virtues can go bad. For example, Jonathan Sanford’s
recent monograph, *Before Virtue*, defends Aristotle’s doctrine that “it
is impossible to exercise any virtue, with the exception of technical
skill, wrongly.”[@sanford2015before 163] On this response, virtues are
always good, such that if a particular action or trait turns out to be
bad, then it must not be a virtuous action or trait. The danger of this
response is that it seems like an ad hoc “No True Scotsman”
fallacy.[^42]

It seems to me Foot argues that virtues cannot go bad while trying to do
justice to the worry that the stipulation is ad hoc. Her solution is, I
think, ingenious. She makes an analogy to poisons and solvents:

> It is quite natural to say on occasion ‘P does not act as a poison
> here’ though P is a poison and it is P that is acting here. Similarly
> courage is not operating as a virtue when the murderer turns his
> courage, which is a virtue, to bad ends. Not surprisingly the
> resistance that some of us registered was not to the expression ‘the
> courage of the murderer’ or to the assertion that what he did ‘took
> courage’ but rather to the description of that action as an act of
> courage or a courageous act. It is not that the action could not be so
> described, but that the fact that courage does not here have its
> characteristic operation is a reason for finding the description
> strange.[@foot2002virtues 16]

An agent’s commission of an otherwise virtuous action may be a mistake
*for that agent* at that time.

A second, slightly different response is to allow that some virtues can
go bad under certain conditions; and so individual virtues although
*usually* or *typically* operating toward good ends *can* be corrupted
in the absence of a higher-order executive virtue that coordinates
virtues toward their proper ends and recognizes if and when a particular
virtue has limits. That executive virtue is usually taken to be
practical wisdom. An apparently courageous act may serve depraved ends
if we allow that the apparently courageous person acted unwisely *in
this case*. On this second response, all the virtues depend for their
successful execution on the coordinating management of practical wisdom.
We might categorize John McDowell’s account as an example of this type.
In “Virtue and Reason” he argues that all virtues are, in the end,
examples of practical wisdom. And since practical wisdom, by definition,
cannot go bad, the problem of *virtues going bad* does not arise.
“Virtues” benefit their possessor since they amount to the kind of
wisdom by which one is able to live a good life. (I shall dispute
McDowell’s conflation of all virtues with practical wisdom in chapter
5.)

A third response is to expose a hidden assumption in the problem. There
are admittedly putative cases of virtues going bad; the critic alleges
that *any* traditional virtue might turn out to be bad in some
circumstance. To assert that *no traits* are always good would be to beg
the question in favor of moral nihilism or relativism.

It seems to me the safest course is to insist on the following minimal
stipulation: almost all virtues almost always benefit their possessor.
By this stipulation, any theory of virtue according to which virtues
turn out to harm their possessor *overall* is simply ruled out. At the
same time, the stipulation has three strengths. First, it allows us to
take seriously cases wherein a seeming virtue seems to harm its
possessor or others; perhaps, if a trait is not beneficial, then we have
simply misjudged it as a virtue. Secondly, it allows us to concede the
intuitive objection that some virtues (honesty) might be corruptible by
the presence of overwhelming vices (such as cruelty) or that individual
virtues (such as courage) may be *costly* and so cause their possessor
pain or discomfort – many a just politician has passed up personal
wealth by refusing bribes. Thirdly, this minimal stipulation agrees with
Foot that at least one virtue – practical wisdom – is *always* operative
to good ends. I shall discuss this problem a bit more below. For now, I
conclude that almost all virtues, if they are truly virtues, are almost
always beneficial.

Plato’s requirement is that virtues benefit their possessor. I have
allowed that they may cause their possessor to lose out on money, fame,
or comfort. A related query is whether virtues are supposed to benefit
*others* as well or only their possessor. For some virtues, the answer
is clearly *both*. Still, aren’t some individual virtues *more*
beneficial to one party, possibly at the expense of the other?

The answer is difficult to state systematically. By hypothesis, virtues
are beneficial to *human beings* as a kind, not just this or that
individual. One can approach the thesis that virtues are beneficial to
human beings qua human from two angles. Consider moderation with respect
to alcohol. Such moderation benefits one’s family, one’s community and
so on. The ravages of alcoholism on marriages, children, and extended
families are widely known. So it would seem to be altruistic not to
over-drink. Nevertheless, moderation with alcohol also benefits oneself.
Indeed, parsing up the benefit seems foolhardy. (Who benefits more, your
children or your liver?)

For virtues such as justice or charity, the answer might be less clear,
but the lack of clarity does not damage the account. Foot says, “It is a
reasonable opinion that on the whole a man is better off for being
charitable and just, but this is not to say that circumstances may not
arise in which he will have to sacrifice everything for charity or
justice.”[@foot2002virtues 3] Even so, she finds the alleged paradox
between what we might wish to call “selfish” and “altruistic” virtues
overblown.

Certainly, sometimes life presents us with the opportunity to pursue
only one of two contradicting or apparently irreconcilable goods; my own
good *versus* your good. Sometimes, however, the cases in which virtuous
deeds necessitate the loss of other goods are not so devastating as they
might appear. It might be that, on occasion, it is better (say) for my
family that I sacrifice my health in working hard to earn higher wages;
while on other occasions it is better for my family that I sacrifice
higher wages to keep myself healthy. Even when there is a clear,
irresolvable tension between my good and the good of the group (as when,
say, I must sacrifice my life), we can make sense of the demand of
morality by appealing to what is necessary *for humans* in general. As
Geach says: “Men need virtues as bees need stings. An individual bee may
perish from stinging, all the same bees need stings; an individual man
may perish by being brave or justice, but all the same, men need courage
and justice.”[@geach1977virtues 17] Geach further points out that the
clear contrast between my “inclinations” (e.g., to self preservation) is
largely an artifact of philosophical thinking; many people are
*inclined* both to preserve themselves *and* to obey the moral law.

Some critics have posed an objection to the effect that virtues are what
Kant would call “hypothetical imperatives” – that we only need virtue
*if* we want to be happy. On the contrary, the acquisition of virtue is
a formal necessity for all members of the human race. As the gestating
bee needs to develop its sting in order to realize its life form, we
need virtues *to be human*. If this is right, then everyone has an
obligation to develop virtuous traits such as being moderate, tolerant,
and wise. Consider only practical wisdom for the moment: the obligation
to become practically wise stems not from one’s prior commitment to
happiness but simply from finding oneself to be a human, and hence
subject to a particular form of practical life which, as it turns out,
is perfected or realized by practical wisdom.

A somewhat different critic might accept the analogy between human
virtues and bee stings but point out that, in fact, some bees *don’t*
need stings. For example, considering the common honey bee, only
females, including the queen, have stings; male drones do not. By the
same analogy, could there be humans that don’t need some virtues?
MacIntyre illustrates this objection with respect to promise-breaking.
He asks us to imagine a complex, social species who each perform some
function on behalf of the survival of the whole. However, the society
also includes “free riders” who do not perform any function. He says:

> Such a society would suffer from a natural defect if there were too
> many free riders, but the existence of some free riders would not be a
> defect, and the free-riders are themselves not necessarily defective
> members of the species. For their existence might have the important
> function of making other members of their society and species more
> vigilant in sustaining the practices necessary for the society’s and
> species’ survival and functioning. So it might perhaps be for human
> beings with promise breakers.[@macintyre2002footgeach]

This objection brings out an important distinction between ‘the human’
qua a biological species bearing a common life form and humans qua
members of society playing various social roles. I cannot fully explore
the distinction here. Suffice it to say that the existence of various
social roles with accompanying, role-specific virtues is compatible with
virtues accompanying a universally distributed life form. As Foot
argues: “Human beings do not get on well without [virtues]. Nobody can
get on well if he lacks courage, and does not have some measure of
temperance and wisdom, while communities where justice and charity are
lacking are apt to be wretched places to live, as Russia was under the
Stalinist terror.”[@foot2002virtues 2-3] Notice the generic form of her
statements: “humans” do not get on well. This is compatible with saying
that courage is *especially* necessary for a soldier or a firefighter.
Even so, plumbers, parents, and professors need a basic level of human
courage. And, again, practical wisdom is needed by all who are
physically and mentally capable of acquiring it. MacIntyre’s example
shows how a (virtuous) society *can* sustain the presence of vice-ridden
members without being utterly destroyed; it even supports the surprising
notion that a virtuous society can retain or augment its virtues by
supporting vice-ridden members. It does not do anything to justify the
suggestion that vice-ridden members are ipso facto necessary. For even
if the presence of free-riders were a net benefit to the imagined
society, it is possible for others to play that role, such as the young,
the critically injured, and so on.

Another critic might accept all this and ask: if people *need* the
virtues, and if even “altruistic” or other-regarding virtues benefit
their possessor, is it then egoistic and “selfish” to pursue virtue? Not
at all. Acquiring one’s own virtue is no more selfish than eating one’s
own food and getting one’s own sleep. The pursuit of virtue is
beneficial to the self, but not selfish in the pejorative sense that
usually implies neglect of proper sensitivity to the needs of others.
Furthermore, the charge of egoism assumes that in every case what is
*good for me* is ipso facto *bad for someone else*. We need not assume
this. It may be established, upon reflection, that in some cases what
might be good for me turns out to be bad for someone else, or for
humanity in general, but this must be established case by case. For it
may turn out that what is good for humanity in general is ipso facto
good for me as a human. Take an example: I would argue that various
simple pleasures of life arising from cooking and eating good food, or
strolling through natural beauty, chatting with an old friend, are on
balance good parts of life. But they are not *the only* goods. If they
were the only goods, one might go in for those pleasures and those
pleasures alone. One might construct one’s whole life around them. But
having moderation is a good as well. So a person who enjoys both the
moderate pleasures of life and the moderation of pleasure and pain is
both a better fellow and better person.

In this connection, we should recall the brief argument above that
virtues are intrinsic goods. They are not just traits that *lead to good
consequences* for organisms like us (that too). The recent revival of
virtue consequentialism defines virtues as instrumental goods. For
example, Thomas Hurka argues that virtues have “recursive” value in that
they have some intrinsic goodness in themselves while being a means to
(other) intrinsically good ends.[@hurka2003virtue chapter 1.] Still, I
differ from Hurka, who thinks that virtues are valuable *primarily*
because they are useful to secure other intrinsic goods. Alasdair
MacIntyre agrees that virtues have both kinds of value, but switches the
priority. For example, he is careful to distinguish between intrinsic
and instrumental goods; he says that virtues “enable their possessor to
achieve … goods” of practices, which might sound as if he means virtues
are mere *instruments* to goods. They are instrumental but not *merely*
instrumental to the achievement of goods. They are also *partly
constitutive of those goods.*

In my view, MacIntyre is closer to correct here: being virtuous
constitutes a naturally good state for human beings. The other benefits
that accrue to a virtuous person are of secondary value.

To use a well-worn example, it is fairly uncontroversial that friendship
is a good for practically rational, social animals. Suppose that one’s
*having friends* depends, in part, on one’s *being friendly*. What does
it mean to ‘be friendly’? Being affable is not enough; one must have
some of the traits that make one a good friend: being a good listener,
showing genuine concern for others, rejoicing when a friend’s life is
going well, empathizing when it is not, and so on. Such traits are not
commendable *merely* because they happen to help one to have friends.
Rather, they are commendable because such traits, in part, make one a
good human being. It so happens that, when two people have such traits,
they will be good friends to each other. Good humans make good friends.
And it is better, on balance, to have those traits whether or not
friends are forthcoming. Fortune may place one in a lonely setting:
military posts, solitary jobs, and so on. But as Judith Thomson says, a
virtue is a trait such that, “whatever else is true of those among whom
we live, it is better if they have it.”[@thomson1997right] Likewise,
Philippa Foot says: “let us say then, leaving unsolved problems behind
us, that virtues are in general beneficial characteristics, and indeed
ones that a human being needs to have, for his own sake and that of his
fellows.”[@foot2002virtues 4] While we cannot pretend to have resolved
the notorious tensions between altruism and egoism, we must move on in
the pursuit of a definition of virtue.

Excellent and Corrective Traits
-------------------------------

The second point about virtue is that virtues cause and partly
constitute the excellent functioning of a human being. What is
‘excellence’? The concept of excellence is relative to an object’s
nature and function. The common example is that the function of a knife
is to cut, so an excellent knife *cuts well*. More complex beings have
more complex functions and therefore a more complex kind of excellence.
An excellent guard dog is one that barks loudly, is hostile to
strangers, but remains gentle with friends, and so on. Artifacts receive
their function by design, but even a natural entity such as a dog
receives an artificial function (guarding) by design. It is tempting to
jump to the conclusion that *all* functions are artificial objects of
human invention. On this view, natural organisms (trees, dogs, humans)
have no *inherent* function, and no function at all unless one is
imposed upon it by an agent from the outside.

As I have argued, however, natural organisms have natural functions,
namely to develop fully into what they are. Even without knowing the
full details of its origin, we can empirically discover the telos of an
organism by observing it grow in proper conditions, and discerning
between exemplary and non-exemplary members of the kind. We can learn
that an acorn is a *Quercus alba* (white oak) only by observing and
reflecting upon its development from embryonic stages to maturity, and
by observing the characteristic activities exhibited by mature, typical
members of the species. Likewise, the use of dogs in guarding roles is
not *only* artificial; even before breeding, some dogs are not at all
suited to the task, while others are well suited. We observe that the
natural behavior of some full-grown, healthy dogs is to be more alert,
protective, fierce, or what have you. Breeders and trainers then augment
these natural ends and direct them toward human ends.

A natural inference to draw would be that human beings have a
“function,” howsoever complex, and that a detailed knowledge of this
function is necessary for defining human excellence. I am persuaded by
Geach that it is not necessary to be able to specify in great detail, in
advance, our function. He says:

> … in that way of thinking it makes good sense to ask ‘What are men
> for?’ We may not be so ready with an answer, even a partial answer, as
> when we ask ’What are hearts for?… But Aristotle is right to my mind
> in desiderating an answer – the success in bringing men’s partial
> organs and activities under a teleological account should encourage us
> to think that some answer may be found. Not as quickly as Aristotle
> thought. It does not show straight off what men are for if we know
> that men and men only are capable of theoretical discourse… Consider
> the fact that people of different religions or of no religion at all
> can agree to build and rent a hospital, and agree broadly and what
> shall be done in the hospital. There will of course be marginal policy
> disagreements… But there can be an agreement on fighting disease,
> because disease impedes men’s efforts towards most
> goals.[@geach1977virtues 12-13]

Geach goes on, later in the same book, to argue for a quite particular
conception of the function or telos of humanity. For my purposes, I
remain content to hypothesize a quite general function in accord with
the pattern above. The function of a practical rational primate is, at
least, to become a fully mature practical rational primate – to become,
as Pindar recommends, what we are, having learned what that is. This
quite general function should not be interpreted to mean that virtuous
human beings just sit around “being human” all day; they perform
“characteristic action” typical of the species, whatever that turns out
to be. Just as we cannot define a priori how tall redwoods grow or the
lifespan of an red-toothed shrew, we should not expect that we could
define, a priori, how wise a human specimen can become. Instead, we
should preserve a healthy agnosticism that is open to new possibilities.
Wisdom, like knowledge, is expansive; how many languages can one person
learn? 10? 25? 100?[^43] How widespread can competence with the basics
of quantum physics become? Similarly, how much practical wisdom can one
person acquire in a lifetime? How much practical wisdom can a society
accumulate in a hundred generations? It seems to me that these questions
admit of no obvious, in principle limits.

Still, readers could rightly demand more details. People and societies
disagree; does my account offer any judgment on who is right, or who is
close? My goal here is to lay the foundations, not to build the whole
structure. Nor should we be dismayed at wide and often stubborn
disagreement between varying traditions as to which exemplars best
represent fully mature, practically wise human beings. The inquiry is a
difficult one, and perhaps requires that the inquirer attain to
practical wisdom before being able to properly judge the merits of each
case. I only insist, here, that we do not need to specify at the outset
anything more than that the characteristic actions of practical rational
primates will involve the kinds of virtuous actions and excellent
practical reasoning that I am developing.

That said, it is much easier to spot weak and sickly specimens of a
species. In plants, a well-trained botanist can diagnose *something
wrong* with even an unfamiliar species via tell-tale signs such as
spots, colors, and sickly shapes. Similarly, a competent adult can
diagnose *something wrong* with a hopelessly addicted drug-user whose
habit is ruining his life, or with an incorrigible fool whose life is
tragically cut short by his own recklessness.

A related point is that virtues are corrective. As Foot argues, virtues
become urgent when common vices become tempting: they stand “at a point
at which there is some temptation to be resisted or deficiency of
motivation to be made good.”[@foot2002virtues 8]

It might seem odd that “evil” could be tempting. But examples are all
too easy to supply. Obesity and malnutrition or starvation are both bad
for human beings. The obvious difference is that malnutrition is usually
involuntary while obesity is usually voluntary – few people (though
some) starve themselves but many people (though not all) gain weight by
electing to eat too much when the high calorie foods are available.
Habitually going in for overeating is an example of immoderation.
Immoderation with respect to eating is bad for oneself. So at the point
where the temptation to embrace the bad comes in, the possibility of
virtue comes in as well.

Foot’s discussion of Kant on this point is instructive here. She
paradoxically objects to a statement of Kant that *only* “actions done
out of a sense of duty” have moral worth and at the same time agrees
with Aristotle that “virtues are about what is difficult for men.” How
can we make sense of this paradox?

Consider Kant’s problem of the happy philanthropist. This problem is the
troubling and dissonant conclusion that if a very generous
philanthropist gets great pleasure out of helping others then such
actions display no moral worth. Surely a commonsense moral judgment
would accord moral worth to the very fact that the philanthropist
*enjoys* doing what is good. The philanthropist doesn’t grit his teeth
and do good. Gritting one’s teeth and doing good is what Aristotle would
call mere *continence*; the virtuous philanthropist enjoys the activity
in accord with virtue. Ease or fluency in performing virtuous activity
is baked in to the definition of the virtuous person.

Kant’s error, according to Foot, is in failing to distinguish that which
is “in accord” with virtue from that which is *virtuous* full stop. It
may be, for example, that a novice tennis player makes an expert shot
while remaining merely a novice. The hit is “in accord” with excellence
but is not, in this case, an instance of excellence – only beginner’s
luck. In her self-love example, Foot points out that there is no virtue
required to eat one’s breakfast and avoid life-threatening danger, but
there may sometimes be cases where self-love is a duty – even a
difficult, painful duty. She says, “sometimes it is what is owed to
others that should keep a man from destroying himself, and then he may
act out of a sense of duty.”[@foot2002virtues 13] So the solution to the
happy philanthropist problem is this: if the philanthropist really does
have character such that he is delighted helping others, he is morally
praiseworthy *because he has worked to achieve that character*. As Foot
says:

> For charity is, as we said, a virtue of attachment as well as action,
> and the sympathy that makes it easier to act with charity is part of
> the virtue. The man who acts charitably out of a sense of duty is not
> to be undervalued, but it is the other who most shows virtue and
> therefore to the other that most moral worth is
> attributed.[@foot2002virtues 14]

Since charity is a “virtue of attachment” (I should say “affection”),
the feelings of the philanthropist count in favor of proving the
presence of a virtue.

Common sense would judge that a philanthropist who persists in virtue
even when he does not enjoy giving is also praiseworthy. Foot explains
this too. She allows that it may take greater virtue for a man to
*persist* in his philanthropy *even when* it brings him no delight.

> Only a detail of Kant’s presentation of the case of the dutiful
> philanthropist tells on the other side. For what he actually said was
> that this man felt no sympathy and took no pleasure in the good of
> others because ‘his mind was clouded by some sorrow of his own’, and
> this is the kind of circumstance that increases the virtue that is
> needed if a man is to act well.[@foot2002virtues 14]

For someone who has acquired a kind of immunity to some kinds of
temptation is through sustained effort and in many small victories is,
ipso facto, especially admirable. Virtues are indeed corrective of
tempting vices and tempting moral errors. However, the presence of
temptation is not a necessary condition for the presence of a virtue.

I would like to respond to two possible worries some readers may have.
The first worry is that defining virtue as “beneficial” or “positive” by
definition is circular and therefore empty. Suppose we define “boldness”
as *doing hard things* and “courage” as doing hard things when it is
good. Boldness is, so to speak, value neutral. One can be bold in
wrongdoing or bold in doing well. If courage is just boldness in doing
good, then the affirmation that ‘courage (doing hard things when it is
good) is good’ would appear to amount to the trivial revelation that
‘good things are good.’ And most (if not all) tautologies are trivial.

This is an important objection, but it misses the point. These ethical
propositions are not tautologous but are so widely and commonly accepted
as to be easily mistaken for tautologies. If we define “kindness” simply
as “a disposition of treating others *in a good way*” then it appears
that “it is good to be kind” amounts to the same tautologous proposition
“it is good to be good.” But kindness is *not* best defined simply as
*something good*. Instead, we must realize that some ethical
propositions are synthetic, yet so widely believed and so widely
affirmed that they appear to be tautologous. Some philosophers argue
that this widespread, near universal belief is a sign that these
propositions are self-evidently true. For instance, Russ Shafer-Landau
says:

> It seems to me self-evident that, other things equal, it is wrong to
> take pleasure in another’s pain, to taunt and threaten the vulnerable,
> to prosecute and punish those known to be
> innocent…[@shafer2003moralrealism, chapter 11]

Peter Geach argues that just because an ethical conclusion is virtually
un-revisable doesn’t mean it is a content-less
tautology.[@geach1977virtues, Chapter 1] That kindness is good is rather
a hard-won insight. Only by reflection can we know that humans have a
nature and a species-specific kind of flourishing. Only by reflection
can we learn which character traits are conducive to the realization of
our life form while others are conducive to its stultification. (I
return to this issue in chapter 5.)

A second worry is that this account of virtue sets the bar for virtue
too high. I agree with Foot on this point. She denies the suggestion
that *only* those who are completely virtuous are virtuous at all. There
is at least one virtue that always operates as a virtue, namely,
practical wisdom. While it might make some sense to speak of “foolish
courage” (recklessness) or “foolish moderation” (prudishness) it makes
no sense to speak of “foolish wisdom.” Knowledge may and does contribute
to wicked actions, but wisdom (by definition) entails a proper
application of knowledge. Since wisdom always operates as a virtue, we
admire wisdom perhaps most of all.[^44] Secondly, we do admire virtues
when they all appear in a remarkably virtuous person and when only one
or two appear in a partially virtuous person. Foot says:

> There are some people who do possess all these virtues and who are
> loved and admired by all the world, as Pope John XXIII was loved and
> admired. Yet the fact is that many of us look up to some people whose
> chaotic lives contain rather little of wisdom or temperance, rather
> than to some others who possess these virtues. And while it may be
> that this is just romantic nonsense I suspect that it is
> not.[@foot2002virtues 17]

Foot believes that even those whose overall life is a mishmash of
virtues and vices are admirable. My interpretation of this sentiment is
that such are admirable insofar as they demonstrate some excellent
qualities.

Acquirable
----------

A fourth attribute of virtues is that they are acquirable. MacIntyre
above defined virtues as *acquired* human qualities; I would only modify
this definition to “acquirable,” because not everyone has all the
virtues and some people never acquire some virtues. *How* virtue is to
be acquired is an age-old theme I shall not explore.[^45] Yet even
without stating *how* virtues are acquired, it is still essential to see
that they must be *acquirable.*

On my view, we are ultimately responsible for our ‘moral’ traits. We can
voluntarily lose them or attain them by sustained intentional effort.
For example, Foot thinks virtues are revealed not only by a person’s
abilities but by her *intentions*. What are intentions? She argues that
the ‘will’ or practical reason must be understood in its broadest sense,
“to cover what is wished for as well as what is
sought.”[@foot2002virtues 5] Considered thus broadly, practical reason
(or the will) contrasts with one’s fortune and luck. Call “fortune” all
those features of one’s life and character that are fixed prior to or
independent of practical reasoning. Most basically, all of us are
practical rational primates by fortune. We all exist in a time and place
in history, with a genetic identity derived from our parents, and grow
up in a culture and tradition we receive from our parents, guardians,
friends, and so on. As we become adults, we become gradually more
responsible for our own character, our decisions, and our habits. So
perhaps practical reasoning is the process of deciding what to do with
one’s fortune: what long-term projects to pursue and which objects are
worthwhile to obtain, and how to react to the “slings and arrows of
outrageous fortune.”[^46] We ultimately decide whether to become – or
not to become – fully human.

Saying that virtues are acquirable by intentional effort is not
sufficient. We do not judge a person to be virtuous even if he is a
well-intentioned nincompoop who always harms when “helping.” Neither do
we only judge the result of a person’s action, for we sometimes
exculpate a failing performance in part because the person *meant well*
– the exculpation might be called for when circumstances were not
favorable, chances of success were low, etc. Instead, a virtuous action
is one that aims at the right thing in the right way, and flows out of a
person’s acquired character. Foot attempts to capture the point that we
admire someone who not only does the right thing but who has conditioned
himself to do the right thing fluently and almost instantly. She quotes
from *A Single Pebble*, a John Hersey novel in which a man saves a boy
from drowning:

> It was the head tracker’s marvelous swift response that captured my
> admiration at first, his split second solicitousness when he heard a
> cry of pain, his finding in mid-air, as it were, the only way to save
> the injured boy. But there was more to it than that. His action, which
> could not have been mulled over in his mind, showed a deep,
> instinctive love of life, a compassion, an optimism, which made me
> feel very good.

Foot’s comment is this:

> What this suggests is that a man’s virtue may be judged by his
> innermost desires as well as by his intentions; and this fits with our
> idea that a virtue such as generosity lies as much in someone’s
> attitudes as in his actions. Pleasure in the good fortune of others
> is, one thinks, the sign of a generous spirit; and small reactions of
> pleasure and displeasure are often the surest signs of a man’s moral
> disposition.[@foot2002virtues 5]

I find this analysis convincing. The outward behavior (the swift
response) discloses not only the savior’s intentions and attitudes but
something even deeper, such as settled dispositions that can be betrayed
in the smallest facial expressions or the most “instinctive” gut
reactions. To capture a similar point in a slightly different way,
consider Hursthouse’s argument that virtuous dispositions are
“multi-track” dispositions. She says:

> A virtue such as honesty or generosity is not just a tendency to do
> what is honest or generous, nor is it to be helpfully specified as a
> “desirable” or “morally valuable” character trait. It is, indeed a
> character trait – that is, a disposition which is well entrenched in
> its possessor, something that, as we say “goes all the way down”,
> unlike a habit such as being a tea-drinker – but the disposition in
> question, far from being a single track disposition to do honest
> actions, or even honest actions for certain reasons, is multi-track.
> It is concerned with many other actions as well, with emotions and
> emotional reactions, choices, values, desires, perceptions, attitudes,
> interests, expectations and sensibilities. To possess a virtue is to
> be a certain sort of person with a certain complex mindset. (Hence the
> extreme recklessness of attributing a virtue on the basis of a single
> action.)[@hursthouse1998virtue]

There is a clear similarity, I think, between Hursthouse’s notion of a
multi-track disposition and McDowell’s notion of perceptual sensitivity.
To be sensitive to a range of requirements for action involves one’s
emotions, beliefs, habits, and so on. Virtue is the excellence of
rational practice and practical reasoning. Practical reasoning is the
process of acquiring new traits one does not have but potentially can
have (or of shedding old traits one has but can potentially lose).

I have asserted that virtues are in principle acquirable for human
beings. As stated, this assertion presents us with numerous puzzles. For
example, some skills are acquirable but do not seem to be moral virtues.
And some excellences seem to be instances of non-moral natural goodness
but are not acquirable. How then can we distinguish moral excellence
from skill or strength (which are mostly acquirable rather than inborn)
as well as from physical beauty or natural intelligence (which are
mostly inborn rather than acquirable)?

One reason these puzzles arise is that there exists a terminological
disconnect between the older understanding of morality and the usual
modern understanding. (I shall attempt to disentangle the various senses
of the term ‘moral’ in chapter 5.) On the one hand, as Foot explains,
*άρετή* (excellence) for the Greeks refers “also to arts, and even to
excellences of the speculative intellect whose domain is theory rather
than practice.”[@foot2002virtues 2; Cf. @anscombe1958] Likewise,
MacIntyre says, “The word *arete*, which later comes to be translated as
‘virtue,’ is in the Homeric poems used for excellence of any kind; a
fast runner displays the *arete* of his feet (*Iliad* 20. 411) and a son
excels his father in every kind of *arete* – as athlete, as soldier and
in mind (*Iliad* 15. 642).”[@macintyre1984after 122, emphasis added.]
There are many traits (we might call them *skills*) that are beneficial
to their possessor and others. Even if we grant that skills are
goods-of-a-kind and that a virtue is a good of a kind, skills do not
seem to us particularly *moral*.[^47] On the other hand, even the
traditional list of “moral virtues” (Greek: *arete ethikai*; Latin:
*virtutes morales*) do not correspond precisely to *our* “moral
virtues.” The traditional list of cardinal “moral virtues” (including
courage, moderation, practical wisdom, and justice) includes positive
traits we might classify as “self-regarding” (e.g., moderation) as well
as “other-regarding” (e.g., justice), and includes practical wisdom
(*phronesis/prudentia*) which, if we mentioned it at all, we would be
inclined to classify as an intellectual virtue. Finally, not all of the
items on a comprehensive list of positive qualities (e.g.,
unselfishness) obviously correspond to one of the classical virtues. So,
we ought not to assume that the terms ‘excellence’ or even ‘moral
excellence’ can be a short-cut for understanding the concept of virtue.

The first step toward untangling this puzzle is to observe that skills
are indexed to practices and social roles. Virtues are indexed to our
life form. Skills are only needed by those who undertake those
practices, but virtues are needed by all. A quick wit is necessary for
being a comedian; courage is needed for being a human being. Keen
eyesight and reliable memory may contribute to a pleasant life and
success in various pursuits, but the cardinal virtues are necessary for
success in *any* worthwhile human endeavor.

This response poses a new problem: Suppose Smith and Jones have grown up
in very different cultures with very different kinds of parents and very
different opportunities. Both are, so to speak, front-loaded with
virtuous or vicious habits. Do they then have no chance to acquire new
virtues or shed vices? Or even if traits that are initially inculcated
in a child by parenting, education, and tradition may be modified later,
doesn’t their initial reception break down the dichotomy between what is
in or out of one’s control?

It is true that for the first decade (or two?) we are not primarily
responsible for our own training and formation. However, unless illness
or injury interrupt it, part of the normal process of childhood
development is the gradual transferring of responsibility from
caretakers to child. Without having to pin down exactly when one becomes
an adult fully responsible for oneself, we can put it this way: one is
morally responsible for the character and mind one has *by the end* of
life, rather than the beginning. Virtues and vices are first inculcated
in a child by fortune and tradition and only later modified by that
individual’s own initiative. On a related note, MacIntyre agrees with
Aristotle that virtues are “natural” for humans. More exactly, Aristotle
taught that virtue is *in accordance with* nature but not *by nature*.
That is, virtues are not *natural* in the sense that natural attributes
such as hair color are ‘automatic’ but they are natural in the sense
that they are *proper* to human beings, they are formal features of
practical, rational animals. Virtuous traits are a normal psychological
result of cultivating excellence within particular human practices.

It is quite possible that Smith received many of the benefits of good
fortune while Jones suffered terrible fortune. Let us grant the earlier
points, that (1) they do not need the same set of skills if they won’t
perform the same social function and that (2) they both need the same
“moral skills” essential to any human life, such as relating to their
friends and family, cultivating their talents, facing challenges bravely
and negotiating difficult decisions with wisdom. Are they equally
responsible to acquire all the same virtues? As a matter of fact, few
people acquire all or even many of the virtues. But all who are capable
of practical reason can and must acquire some. Still, are all virtues
acquirable by all? I think an adequate answer to begin with is the
motto, ‘*one should acquire as much of as many virtues as possible.*’

Let me unpack this. It is not necessarily the case that every person can
acquire every virtue equally. Aristotle taught that “affability” was a
virtue. Modern readers might be inclined to smile at the notion that
inborn friendliness and cordiality make one somehow *morally* better
than their melancholic counterparts. I do not think he was completely
wrong in judging this trait to be humanly important. Social interactions
are an optional part of most human lives, and even if we do not
typically classify affability as a *moral* virtue we do tend to admire
those who have a proper amount of affability and blame those who are
excessively aloof or excessively cloying. If affability is indeed a
human norm, are some human norms merely commendable but not obligatory –
not “perfect duties” in Kant’s sense?

The answer requires some sensitivity to circumstance. A family suffering
from undernourishment needs to practice moderation in a very different
manner than a wealthy family experiencing surplus. Nevertheless, if it
is possible to discover fundamental human virtues (like moderation and
practical wisdom), then it is possible to discover virtues the
acquisition of which is incumbent upon everyone regardless of their
circumstances. Indeed, practical wisdom is needed by all to help
identify which virtues and skills are needed in their circumstances. It
would be practical folly to take adverse circumstances as an excuse not
to acquire any particular virtues.

Relatedly, I want to preempt the suggestion that those who are, say,
natively affable or intelligent are *morally* superior to those who are
natively solitary or unintelligent. Just as some are natively more
physically healthy than others, we can affirm that nature distributes a
diversity of gifts. There is no “fault” in being less fortunate. We have
to remember the lesson that Anscombe taught us: the peculiarly moral
“ought” in virtue ethics is not the same as the verdictive “ought” of a
divine law.[@anscombe1958] We ought to become as virtuous and wise as
possible because that is our natural end. The failure to do so is a
natural evil. For neo-Aristotelians, virtues are not obedience to
categorical imperatives or divine commands; they are ways of developing
one’s emotions into the likeness of a true human being.

But again, at some point of natural maturation we become responsible for
acquiring whatever virtues we lack, even within the limitations of our
own aptitudes. And most people in the world will not write books, and so
the excellence intrinsic to academic practices are not necessarily
*human* virtues; however, every human being in the world is a practical,
rational primate and has biological parents and so needs the excellence
intrinsic to the practice of human life. Even orphans and street urchins
live in some form of community.

I must return to the problem of Smith and Jones above. Smith’s good
fortune consists not only in the enjoyment of positive external
circumstances but the acquisition of some moral virtues from a young
age. Jones is less virtuous even before they both reach an age of
self-responsibility. How is this fair? First, fortune is certainly not
fair. This kind of unfairness cannot be totally eradicated. Secondly,
even if some good traits may be inculcated at a young age, rational
adults must take responsibility for rendering them secure. Likewise,
even if some negative traits may be inculcated at a young age, rational
adults must take responsibility for changing them.

We may praise or appreciate those who enjoy good fortune; but we
*admire* those who have taken what gifts of fortune they have and put
them to good use. We especially admire those who have overcome
misfortune to acquire excellence and wisdom against the odds. Compare,
for example, the crowds cheering for Olympic runner Derek Redmond when
he is winning the gold medal with the crowds cheering for Derek Redmond
finishing last after his hamstring tore and his father helped him to
cross the finish line. There have been many gold medal winning races
that millions of people have witnessed and forgotten. But this race,
when an otherwise naturally talented and well-trained athlete finished
*last* that remains forever etched in the memory of millions more. It’s
not just the unbridled emotion Redmond displayed in that moment which so
touches viewers; it’s the obvious love from his father shown in
supporting his son’s commitment to finish the race, even dead last.
Likewise for Smith and Jones. Suppose that by the time Smith comes of
age she is moderate, courageous, and relatively wise while Jones is
immoderate, cowardly, and foolish. At some point, both agents take their
own character in hand and practically reason about how to live. Jones
would be all the more admirable if he became virtuous against the odds.

We can make a final comment about a case like Smith and Jones where
their respective levels of virtue and vice are unequal even from a young
age. Rather than absolving us of responsibility for our own character,
this possibility underscores the importance of moral and intellectual
education. In some very key respects, the acquisition of virtues and
vices with which we begin adult life depends upon our
education.[@wood2014prudence] The beginning of human life, like the
beginning of any organic life, is the foundation for all that follows.
When a mother drinks heavily or uses cocaine while pregnant, the child
is going to suffer the negative consequences for the remainder of his
life. When a child is abused – emotionally, verbally, physically, or
sexually – by her parents, the psychological cost is meted out across
the entire life and across generations. By the same token, when a mother
eats healthily and follows all the doctor’s orders while pregnant, the
child is going to reap the positive consequences for the remainder of
his life. When a child is given love, approval, empowerment, discipline,
by her parents, the psychological gains are meted out across the entire
life and even across generations. We should never give in to the
temptation to think that the cultivation of virtue is simply a business
for adults (least of all adult professional academics) to argue for and
against. It is the business of societies and families to do or fail to
do every day. \newline
\indent By calling virtues *acquirable* I mean to argue that certain
fundamental moral and intellectual virtues are obligatory on all
adequately mature and functional human adults – such as those given
emphasis by the Aristotelian tradition, such as courage, justice,
moderation or self-control, and practical wisdom. But my account makes
space for the commonsense thought that some traits (say, affability) are
not obligatory for *everyone* to acquire equally. Furthermore, it may
very well be that particular virtues – like skills – are especially
necessary (or especially optional) for people in particular social roles
or stages of life. Nevertheless, practical wisdom is one virtue that is
especially important, because it is obligatory on all potentially
practical rational primates – namely, all human beings – and because
practical wisdom enables one to adjudicate which and to what extent the
other virtues are needful in one’s own case.

Rational and Practical
----------------------

The fourth attribute I would like to discuss is this: virtues are those
traits that enable excellence in rational practices and practical
reasoning. The remainder of this chapter focuses on these two related
concepts. In this pursuit, I shall first summarize MacIntyre’s notion of
“practice,” which is both an interesting concept in its own right and
also crucial to MacIntyre’s account in *After Virtue*.

What is a practice for MacIntyre? A practice is a social activity aimed
at defined ends. For example, MacIntyre mentions farming, chess, and
political activity, among other examples. (We commonly speak of
“practicing” medicine in this sense.) A practice is not merely a
reflexive action such as scratching an itch, nor merely a single,
discrete, intelligible action such as pulling a weed. It is, rather, an
intelligible set of actions undertaken in pursuit of a pre-determined
end. Practices not only have pre-determined ends, but embodied
histories. Leading MacIntyre scholar, Christopher Lutz, highlights four
aspects of MacIntyre’s famous definition of practice. A practice is:

> [1] a complex social activity that [2] enables participants to gain
> goods internal to the practice. [3] Participants achieve excellence in
> practices by gaining the internal goods. When participants achieve
> excellence, [4] the social understandings of excellence in the
> practice, of the goods of the practice, and of the possibility of
> achieving excellence in the practice are systematically
> extended.[@lutz2015]

We could use any number of illustrations of practices to unpack these
four aspects. I shall use a practice in which I have personal
experience: secondary school education. The practice of educating young
people is a complex social activity that is aimed at certain goods. It
has its own history and its own standards of excellence. A secondary
school teacher is engaged in a series of activities aimed at giving
children a body of knowledge and skills they need to become functional
adults in society, whether by getting a job, starting a business, or
advancing to higher stages of education. Secondary education might have
other *de facto* purposes as well. Many parents send their children to
school to socialize them in a community of peers and authorities, or to
afford them opportunities for recreation, art, clubs, or simply to get a
break from parenting. For the sake of simplicity, I shall focus on what
seems to me the primary goal of education, which is education (in
knowledge) and training (in skills) needed for becoming a functional,
legal adult.

Secondary education in the U.S. is a practice. It has a history (or a
set of histories) dating back to the colonial era, with a significant
shift in the 1910-1940s when secondary schooling became the rule rather
than the exception. The practice has its own standards, both legal and
“best practices” passed from mentor to student teacher. It pretty
obviously has standards of excellence according to which most educators
are average, some poor, and some excellent. An educator who wants to
join that profession will be enculturated with that history, taught
those standards, and given a chance (usually by trial and error) to
become a good teacher.

Lutz’s first condition is met, since [1] teaching is an inherently
complex *social* activity, in that teachers cannot be teachers without
students, and (usually) do not teach in isolation but in community with
colleagues and administrators and parents. [2] Secondary education qua
practice enables teachers to gain the goods “internal to the practice,”
namely students who are educated enough to be ready for legal adulthood
– for a job or college. [3] Good teachers are those that demonstrate the
ability reliably to produce educated students, sometimes in the face of
incredible obstacles. And [4] the criteria for what makes schools and
teachers good usually has a *history* and social context that is being
“extended” across generations. Good schools recruit and train good
teachers; good teachers train the next generation of good teachers, and
so on.

One other feature of MacIntyre’s concept of practice deserves comment.
He defines virtues with reference to goods *“internal to”* practices,
and also fashions the same contrast between ‘internal’ and ‘external’
goods as one between ‘goods of excellence’ and ‘goods of
effectiveness.’[^48] What is the point of this distinction?

The “goods of excellence” of a practice are those that *necessarily*
contribute to success within a given practice. In secondary education,
success is defined by, say, graduation rates, retention of information,
high test scores, acceptance to good colleges, low drug use, and so on.
The profession-specific virtues needed include understanding (to stay
patient with struggling students), affability (to keep rapport),
articulateness (to present material effectively), and so on. More
general virtues needed include honesty, integrity, courage,
faithfulness, and so on. Without these, *teaching* may be possible but
*teaching well* is impossible.

By contrast, goods of effectiveness are those that might fit with the
practice but are not *necessary* for achieving the end of that practice:
high pay, an excellent teacher lounge, a short commute to work, and so
on. Mere efficiency in attaining such external goods does not entail the
presence of a virtue. In fact, the desire to pursue such goods *instead
of* the goods of excellence is not a neutral desire — it is a
*temptation.* Virtues are needed to overcome those temptations and to
succeed according to the standards of the practice itself.[^49]

It is important to hold in mind both *practices* and *practical
reasoning*. The virtuous agent does not merely act well (without
reasoning) nor merely reason well (without acting). I would suggest that
McDowell is wrong to assert that *all* of virtue is by definition a kind
of practical knowledge or disposition. Rather, *some* virtues are
excellences in practical reasoning but others are excellences in
rational practice. (I offer a full critique of McDowell’s conception of
moral and practical reasoning in chapters 5 and 6.) Acting takes a
moment of time; the cultivation and maintenance of habits takes a longer
period of time; but living a good life takes a lifetime. So it is
impossible to give an adequate account of virtue without considering
one’s life as a whole. Practical reasoning is the name we give to that
whole complex process by which we undertake to direct our own lives.

Turning again to *After Virtue*, MacIntyre’s first stage defined virtue
in relation to practices. His second stage goes further to include the
whole of life.[@macintyre1984after, chapter 15] He says that “without an
overriding conception of the telos of a whole human life, conceived as a
unity, our conception of certain individual virtues has to remain
partial and incomplete.”[@macintyre1984after 202] MacIntyre undermines
the notion that the virtues which enable success in practices can be
sufficient for an account of virtue in general. He argues that we need
to “envisage each human life as a whole, as a unity, whose character
provides the virtues with an adequate telos.”[@macintyre1984after 204]

Envisaging human life in this way faces serious obstacles. Answering
them requires doing a bit of philosophy of action. The two kinds of
obstacles MacIntyre cites are (a) social and (b) philosophical. The
social obstacle is the fragmentation of modern life: “work is divided
from leisure, private life from public, the corporate from the personal.
So both childhood and old age have been wrenched away from the rest of
human life and made over into distinct realms.”[@macintyre1984after 204]
Just as the temporal segments of life are fragmented into bits (one
thinks of the inherently patronizing talk of “senior citizens” compared
from the older, inherently reverent talk of “elders”), so also the
various projects and pursuits of life are partitioned, labeled, and
cordoned off. On this fragmented view of life, the self’s social roles
are so many conventions masking the “true” underlying nature of the
self. This presents a puzzle: how could virtues arise to the level of
excellent dispositions for *humans as such*? They would have to be
dispositions applicable in personal, private, and business spheres, in
young, middle-aged, and old age, etc.

The philosophical obstacle is the tendency to atomize “complex actions…
in terms of simple components.”[@macintyre1984after 204] MacIntyre’s
argument here is highly significant. He begins by analyzing the way we
might answer a simple question such as: “what is he doing?”

> One and the same segment of human behavior may be correctly
> characterized in a number of different ways. To the question ‘What is
> he doing?’ the answers may with equal truth and appropriateness be
> ‘Digging,’ ‘Gardening,’ ‘Taking exercise,’ ‘Preparing for winter’ or
> ‘Pleasing his wife.’[@macintyre1984after 206]

The first fact to notice is that each of these answers picks out
different aspects of the agent’s action: intentions, intended
consequences, unintended consequences, etc. And, importantly, each of
these answers places the simple atomic action within a narrative. The
action is situated in an “annual cycle of domestic activity,” in a
hobby, in a marriage, and so on – each with its own history and
“setting.”

The second fact to notice is that the answers to a similarly simple
question “Why is he writing a sentence?” might be situated in different
time horizons: immediately, he is writing to finish his book; but also
he is contributing to a philosophical debate; but also he is trying to
get tenure.[@macintyre1984after 207] The upshot of these reflections is
that individual actions abstracted from their context are only
intelligible if they are “ordered both causally and temporally… the
correct identification of the agent’s beliefs will be an essential
constituent of this task.”[@macintyre1984after 208] MacIntyre’s
astonishing conclusion from these innocuous premises is this: “there is
no such thing as ‘behavior,’ to be identified prior to and independently
of intentions, beliefs and settings… Narrative history of a certain kind
turns out to be the basic and essential genre for the characterization
of human actions.”[@macintyre1984after 208] MacIntyre scholar Stanley
Hauerwas argues that the central point in *After Virtue* is that “the
concept of an intelligible action is a more fundamental concept than
that of an action.”[^50] This is such a significant insight because it
shows how individual actions, like individual words, are intelligible in
the context of larger discrete units of action, such as practices and
projects. And, in some sense, the actions one performs within a practice
find their intelligibility not only in practices but in the narrative of
a whole human life. The same is true for verbal contributions to a
conversation: Each word and sentence and speech within the conversation
contributes to an unfolding narrative with a history and a telos,
without which statements are random and unintelligible. MacIntyre
continues:

> But if this is true of conversations, it is true also *mutatis
> mutandis* of battles, chess games, courtships, philosophy seminars,
> families at the dinner table, businessmen negotiating contracts – that
> is, of human transactions in general. For conversation, understood
> widely enough, is the form of human transactions in general.
> Conversational behavior is not a special sort or aspect of human
> behavior, even though the forms of language-using and of human life
> are such that the deeds of others speak for them as much as do their
> words. For that is possible only because they are the deeds of those
> who have words.[@macintyre1984after 211]

Clearly these are weighty matters. Though more could be said, we have
arrived at the supports needed for building the second stage of his
account of virtue: the unity of many practices into a single whole. He
says: “The unity of a human life is the unity of a narrative
quest.”[@macintyre1984after 219]

Naturally, to be on a quest is to strive for a goal, even if one fails
to reach the goal. The goal, he says, is to quest for “*the* good” (as
one understands it at the beginning of the quest). But the conception of
*the* good can grow or morph along the way. How do the virtues relate to
this quest?

> The virtues therefore are to be understood as those dispositions which
> will not only sustain practices and enable us to achieve the goods
> internal to practices, but which will also sustain us in the relevant
> kind of quest for the good by enabling us to overcome the harms,
> dangers, temptations and distractions which we encounter, and which
> will furnish us with increasing self-knowledge and increasing
> knowledge of the good. The catalog of the virtues will therefore
> include the virtues required to sustain the kind of households and the
> kind of political communities in which men and women can seek for the
> good together and the virtues necessary for philosophical enquiry
> about the character of the good.[@macintyre1984after 220]

The virtuous person is sustained by his virtues on the quest toward the
good. Vices not only render difficult or impossible in the achievement
of the good; vices can obscure one’s assessment of what is good and what
is evil.

I can concede that the “quest” of a Stalin or a bin Laden began with
good intentions. It is even important to note that the wicked tyrant
cannot achieve the most horrifying evils and could not come about
without the presence of auxiliary virtues, such as courage and resolve.
Just as a den of thieves cannot survive without at least some honor, a
wicked regime cannot survive without at least some loyalty and
patriotism. Socrates says that the same foolishness and vice that is
laughable in the weak is dreadful in the powerful. The more thoroughly
vicious characters cause less damage because their evil remains petty.

Traditional and Social
----------------------

The fifth and final attribute of virtue is this: virtues enable the
health and progress of whole social traditions. In other words, virtues
are personal but not individualistic. Rather, virtues are instances of
natural goodness for *humans* – and humanity is naturally social. This
is just what we should expect if, as I argued in chapter 3, the
practical rationality that characterizes the human primate is defined in
part by sociality: humans are born into families and learn to speak the
language of their society. Making this case will require a detailed
discussion of MacIntyre’s concept of tradition and practical reasoning.

The crucial third stage of MacIntyre’s *After Virtue* account situates
what has come before in a broader social and historical context. For
MacIntyre, a tradition is, roughly, a “historically extended, socially
embodied argument, and an argument precisely in part about the goods
which constitute that tradition.”[@macintyre1984after 222] I have argued
that practical rationality is the differentia of human nature. Insofar
as virtues depend for their effective operation on the coordinating
management of practical reason, it is of utmost importance that an
individual learn how to practically reason well. This happens, or fails
to happen, in traditions.

Human beings develop their capacity to recognize practical reasons
within a family and society with its own idiosyncratic political,
religious, and philosophical worldview. So, quite plausibly, our initial
de facto set of beliefs, desires, and dispositions reflect the
substantive commitments of our group. As MacIntyre says:

> We, whoever we are, can only begin enquiry from the vantage point
> afforded by our relationship to some specific social and intellectual
> past through which we have affiliated ourselves to some particular
> tradition of enquiry, extending the history of that enquiry into the
> present …”[@macintyre1988whose 401]

The tradition of inquiry we inhabit gives us not only abstract standards
of reasoning but also facts, connections, concepts, and the very
language we speak. Rationality, for MacIntyre, is inclusive of all the
resources by which we judge truth and falsity. Rationality itself as
tradition-constituted and tradition-constituting. The resources I
receive from my tradition are resources I may prune, discard, modify, or
add to. What tradition we are a part of makes a great deal of difference
to how we conduct moral inquiry.

We can make initial sense of the notion that virtues enable the health
and progress of traditions by saying that vices weigh down a whole
tradition and virtues correct and potentially elevate it. MacIntyre
says:

> Lack of justice, lack of truthfulness, lack of courage, lack of the
> relevant intellectual virtues – these corrupt traditions, just as they
> do those institutions and practices which derive their life from the
> traditions of which they are the contemporary
> embodiments.[@macintyre1984after 223]

That said, even if we accept, in outline, the thesis that virtues
sustain and even correct traditions, the problem of relativism rises.
What counts as virtuous is at least partially related to one’s culture,
for every culture purports to provide for its members some minimal
goods. The correct identification of these goods requires practical
wisdom. In *Whose Justice? Which Rationality?*, MacIntyre explicitly
retracts his earlier belief that virtues exist without a unity under
prudence or practical wisdom.[@macintyre1988whose preface, p. x]
Christopher Lutz argues that the consequences of this retraction are
crucial to refuting the charge of relativism.

> …the relativism of *After Virtue* cannot be overcome unless its
> definitions of the virtues are extended to embrace the Aristotelian
> and Thomistic doctrine of the unity of virtue. MacIntyre’s rejection
> of the unity of virtue in *After Virtue* has grave implications for
> the rest of his virtue theory because the rejection of the unity of
> virtue divorces the intellectual moral virtue of prudence from the
> passional moral virtues of courage, temperence, and justice… Prudence
> becomes cleverness…The strength of MacIntyre’s account of practices is
> that the pursuit of excellence in a practice entails the pursuit of
> virtue, but if practices can be evil, and virtues can ‘enable us to
> achieve those goods which are internal to’ such an evil practice, then
> virtues can be anything at all.[@lutz2004tradition 98-101]

By contrast, if virtues are unified, then even though virtues exist only
in the context of practices, “no genuine practice can be inherently
evil.”[@lutz2004tradition 102] Rather, we can make practical rational
mistakes in judging *apparent goods* as genuine goods. The qualities
needed for achieving the spurious goods internal to that “practice”
would not be virtues but only *apparent virtues*.

One pointed illustration is eugenics. Eugenics certainly seems to bear
the markings of a genuine practice. Its apparent good is the
purification of the gene pool for future generations. However, genuine
virtues militate *against* the achievement of that goal. For example,
Lutz cites a story of a virtuous, compassionate doctor who found himself
unable to pursue the program of euthanizing mentally-disabled
children.[@poliakov1979harvest 186-7] We might also recall Huck Finn’s
internal struggle with his “conscience” in Twain’s *Adventures of
Huckleberry Finn*. Huck decides to turn Jim in to the slave owners. He
writes a letter outing Jim, and says: “I felt good and all washed clean
of sin for the first time I had ever felt so in my life, and I knowed I
could pray now.” Yet for all that, after vividly confronting Jim’s
humanity and goodness, he feels the loyalty of their friendship and
wavers:

> It was a difficult situation. I picked up the letter, and held it in
> my hand. I was trembling, because I knew had to make a choice between
> two things, and the outcome of my decision would last forever. I
> thought about it a minute while I held my breath. And then I said to
> myself: “All right, then, I’ll GO to hell” – and tore it
> up.[@twain2014adventures, Chapter 31]

The humor of this passage stems from the tension between the *apparent
good* of treating Jim as legal property and the *actual good* of
treating Jim as an end in himself, as a free man just like any other.
Huck’s virtue (in this case, loyalty or friendship) *cannot* be put to
use in the service of a corrupting practice like slave-trading. Just as
vice subverts institutions and their worthy practices, virtue “subverts”
vicious institutions and unworthy practices. Virtue marks the difference
between the coward who disobeys his commanding officer’s orders because
the obedience would put him at risk of painful death and the courageous
person who disobeys his commanding officer’s order because obedience
would require wrongdoing. Without prudence to discriminate between the
two cases, we lack any resources by which to discriminate courage and
cowardice, between a virtuous resistance and vicious resistance.

The threat of cultural relativism is not fully dissolved by arguing that
individual virtues can subvert the errors in a tradition. What if one’s
tradition is deeply flawed? What if one’s tradition is so fundamentally
mistaken that its vices and errors undermine the possibility that
individual virtues can get a foothold?

This question requires more reflection on the notion of practical
reasoning. In the next chapter, I offer a full account. Here, I must
dispense with one common view that I believe is mistaken. That common
view sets up an opposition between tradition and rational criticism. On
this view, one is either a conventionalist or a subversive. (Define a
subversive as one who goes against (a particular society’s) standard,
traditional, ideology – the “default” view.) The danger of militating
against one’s tradition is that the default view is plausible to most
people, and so the critic necessarily finds him- or herself in the
minority view. On this opposition between tradition and critical
reflection, philosophers are often stereotyped as the subversive type.
Philosophers are not necessarily all subversives; but many subversives
have been philosophers. Nevertheless, I think this whole way of
considering the matter is a mistake.

The first reason is that a tradition is not opposed to rational or
critical reflection – rather a member of a tradition cannot reason
without the resources of that tradition. When we criticize our own
tradition from within, we use what good we enjoy to increase the good.
Secondly, it is idle to speak being “for tradition” or “against
tradition,” for “tradition” says contradictory things. Social Group
Alpha passes along belief A from generation to generation. If A is
false, then rational reflection will turn a philosopher into an
anti-traditional subversive; but if successful, the philosopher might
persuade Group Alpha to believe B instead, and culturally unify with
Social Group Beta. In this case, B will be passed along from one
generation to the next. So the very same philosopher will become a
traditionalist. These labels are about as helpful as asserting that one
is a “newspaperist” who believes whatever is written “in the newspaper.”
The question is, *which one*? Traditions, like newspapers, are a medium,
not a message. The only thing to do, then, is to examine the message —
the content of the tradition.

Still, how is it possible that virtues can sustain what is good in
tradition and enable the successful pruning and improving of the same?
MacIntyre’s answer is that we can rationally adjudicate between
traditions (from within a tradition). We can rationally criticize our
own tradition with the resources available to us. The result may be that
we endorse the truth of the fundamentals thereof, or “switch” from our
primary tradition to a rival.

The path of “switching” traditions begins when one undergoes an
epistemological crisis in which one identifies the inadequacies of a
primary tradition. MacIntyre derived this lesson from his own
experience. As a member of the modern tradition of inquiry – which he
calls “the encyclopedic tradition” – he reflected on the tradition
itself. He gradually discovered its inadequacies and searched for
resources from his rivals. His attempt to trace the root of the mistake
about moral judgments lead him to a mistake at the heart of
Enlightenment modernity. As a social, political, and moral project, the
Enlightenment has been, MacIntyre argues, a failure by its own
standards. Not only is moral discourse largely devoted to moral
disagreement, but it is largely soaked in despair of ever reaching
agreement. Moral discourse with its interminable moral disagreement
retains the rhetorical *trappings* of rationality and objectivity while
denying rationality and objectivity. Neither side wants to give up the
*appearance* of having a dialectical case for its value theory.

One of his most memorable and oft-cited images compares modern moral
discourse to the hypothetical state of scientific discourse in a
post-apocalyptic catastrophe where decaying fragments of intelligible
moral discourse survive, none of which (in isolation) suffices for the
rebuilding of the original, vital discourse.

There are many modern philosophers who have gone into similar crises and
become distrustful of thought, language, and rationality itself; they
join the “masters of suspicion.”[^51] Rather than join the school of
suspicion, MacIntyre took a surprising course. Moved by Thomas Kuhn’s
influential work on the structure of revolution between various
paradigms in the natural sciences,[@kuhn1975structure] he speculated
that a similar structure might obtain in moral revolutions.[^52]

After recognizing the failures of one’s own tradition, MacIntyre points
to a second step: to “exercise… a capacity for philosophical
imagination”[@macintyre1984after, xiii] and identify the resources of a
rival tradition. We must empathetically engage with our rivals as if we
are learning a “second first language.” He says:

> For each of us, therefore, the question now is: To what issues does
> that particular history bring us in contemporary debate? What
> resources does our particular tradition afford in this situation? Can
> we by means of those resources understand the achievements and
> successes, and the failures and sterilities, of rival traditions more
> adequately than their own adherents can? More adequately by our own
> standards? More adequately also by theirs?[@macintyre1988whose 402]

This step of learning a second tradition as a “second first language” in
turn compelled MacIntyre to recover the tradition of virtues. But
virtues are not free-floating moral concepts; they are embedded in a
specific, living, moral tradition. Most prominently within our society,
that is the Aristotelian tradition. The Aristotelian tradition includes
a particular notion of virtue and also of practical rationality.

MacIntyre argues that we should “return” to the Aristotelian tradition
of virtue and practical reason because it is more adequate than its
rivals. We must beware one misunderstanding. Any talk of “returning” is
liable to sound nostalgic. Martha Nussbaum misunderstands MacIntyre’s
argument along these lines.[@nussbaum1989recoiling] In her review of
*Whose Justice? Which Rationality?*, she cites an age-old dilemma
between the social stability afforded by tradition and critical
reflection:

> In the second book of the *Politics*, Aristotle asks whether it is a
> good thing to encourage changes in society. Should people be offered
> rewards for inventing some change in the traditional laws? No, he
> writes, because this would lead to instability and unnecessary
> tampering with what is working well. Should we, on the other hand,
> listen to those who wish to keep ancestral traditions fixed and immune
> from criticism? No again – for if we reason well we can make progress
> in lawmaking, just as we do in other arts and
> sciences.[@nussbaum1989recoiling]

Aristotle’s solution is that it should be *hard but not impossible* to
change societal structures. Strangely, Nussbaum takes MacIntyre to be
reversing Aristotle’s balance. She thinks MacIntyre is emphasizing
social stability at the cost of “recoiling from reason.” But MacIntyre
is emphatically not defending “traditionalism” per se. His definition of
tradition is *progressive*. Tradition is an ongoing, socially-embedded
argument over time, which necessarily entails that moral inquiry is
dynamic – even *modern*. To be traditional is not to be past-oriented;
to be traditional is to be staunchly future-oriented, since the business
of life is not only the pursuit of our telos but the transmission of
everything valuable and precious to the next generation.

MacIntyre elevates the ability to critically reflect on one’s own
tradition and make necessary changes to the level of a virtue, the
importance of which “is perhaps most obvious when it is least present.”
What is that virtue?

> [It is] the virtue of having an adequate sense of the traditions to
> which one belongs or which confront one. This virtue is not to be
> confused with any form of conservative antiquarianism; I am not
> praising those who choose the conventional conservative role of
> *laudator temporis acti*. It is rather the case that an adequate sense
> of tradition manifests itself in a grasp of those future possibilities
> which the past has made available to the present. Living traditions,
> just because they continue a not-yet-completed narrative, confront a
> future whose determinate and determinable character, so far as it
> possesses any, derives from the past.[@macintyre1984after 223]

None of this so far has gone to answer the question: what if one’s
tradition is wrong? How could I, a member of an embodied tradition, ever
get far enough “outside” it to criticize it? This question is
notoriously difficult. The explanation for the difficulty, if not the
solution, is this: We can only think *about* rationality *with*
rationality. We can only reflect upon our thinking process by using our
thinking process. We can only observe rationality *from the outside* by
using rationality *from the inside*. The matter is so complicated
because any argument is self-referential or iterative. When two parties
share an identical conception of rationality, then arduous debate is
unnecessary; when two parties do not share identical conceptions,
arduous debate about a particular issue is liable to shipwreck on the
rocks of metaphilosophical disagreement. As the Greek proverb asks, “if
we choke on food, we drink water to wash it down. If water chokes us,
what shall we drink?”

There can be no quick, ready-made answer to the question of how to
acquire practical wisdom. Answering it is inextricably bound up in the
slow and dangerous process of acquiring the virtue of practical wisdom.
We must be alert to the contours of our own tradition and bold in
considering its weaknesses and failures. We must also exercise
philosophical imagination in learning the contours of rival traditions.
Success is not impossible, but neither is it guaranteed. The only hope
is to practically reason, and to take care to do it well.

Conclusion
----------

Thus far, virtues have come to light as excellent traits belonging to a
fully mature and exemplary practical, rational primate. The virtuous
person does not necessarily enjoy all the blessings of good fortune, but
she does take up all that is given in her fate and put it to the best
possible use. Virtuous people’s lives are remarkable not for what they
are given – any celebrity or cad might be born wealthy or physically
attractive or talented – but for what they do with what they are given.
And practical reasoning is not a simple process different from other
kinds of reasoning or practice; it is the whole complex process by which
we undertake to direct our own lives.

Hursthouse points out that we do not just admire those who survive, but
those who exemplify a *human* form of life: “The human virtues make
their possessor good qua human being, one who is as ordinarily well
fitted as a human being can be in not merely physical respects to live
well, to flourish – in a characteristically human
way.”[@hursthouse1998virtue 208.] This seems right. The exemplary human
being avoids the common and tempting traps one faces along the way of a
normal human life, taking up all the intrinsic and natural urges of
animality (hunger, thirst, the sexual drive, desires for shelter,
comfort, and companionship) into practices that make sense. She works to
acquire those traits that benefit human beings, both oneself and others,
and that enable her to engage in such practices as make sense for human
beings. The definition of “making sense” is admittedly variable
according a person or tradition’s conception of practical reason. And
the notorious difficulty of adjudicating conflicting conceptions has
been briefly noted. While I do not pretend to have offered a resolution
of that difficulty, I have offered two responses: first, an explanation
of why it is difficult; and second, a formula from MacIntyre that might
promise to help a practical reasoner resolve it by carefully working out
a comparison between one’s own conception (with its resources and flaws)
and a rival conception (with *its* resources and flaws). The virtuous
and wise person also navigates his tradition, both sustaining its goods
and correcting its flaws. The virtuous person also takes care to
proactively cultivate virtues in others without unduly short circuiting
her own practical reasoning. On the account thus far developed, these
generics pick out what we are; our moral task is to *become* what we
are.

We flagged three problems but did not fully address them above: (1)
What, if anything, is the human function (ergon)? (2) I said McDowell
mistakes the relation between virtue qua knowledge and virtue qua
rational organization of one’s psychology – including emotions, bodily
urges, physical situation, unthinking habits, and so on – so what is the
relation between practical reasoning and rational practice? (3) Can
virtue go bad? It seems that, without further guidance, otherwise
virtuous traits might operate towards wicked ends, or co-exist with
vices inside an (overall) miserable and vicious person. The solution to
each of these problems requires a clearer account of practical
reasoning. That is my next task.

Practical Reasoning
===================

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{There could be no reasons unless a rational animal has a general conception of its own good, and thus a general sense of how to live.}%
{---\textsc{Jennifer Frey, \begin{em}The Will to Do Good\end{em}, 79.}}
\centering
\end{epigraphs}
“How should one live?” This question is central to neo-Aristotelian
writers such as Bernard Williams, Philippa Foot, Alasdair MacIntyre,
John McDowell, and others. The question is so important, I think, for at
least four reasons. First, the question implies that the questioner is
aware of a dichotomy or distinction between *the way one is in fact
living* and *the way one might live*. As a matter of fact, every capable
adult is already living in a particular way. I take it for granted that
most people learn to live in a particular way from their culture and
family of origin, while also trying to satisfy more or less their own
idiosyncratic preferences. But a normal part of human life is pausing to
reflect on one’s own motives, methods, means, and ends. A crisis can
trigger such reflection: what is wrong with my way of life, my values,
and/or my choices? And exposure to other people – be they friends,
fictional characters, or historical figures – who seem extraordinarily
happy can trigger such reflection: what do they know that I do not? What
are they doing that I am not?

Secondly, the “how should one live?” question assumes that there are
good human lives and bad human lives. I hope that it is uncontroversial
to point out that some of the members of our race are fools. (I leave it
to the reader to supply illustrations.) If there are ways one
*definitely should not live*, then there is at least a way or set of
ways one *should* live. Even if it is difficult to answer the question
of how one should live, we should not be fully skeptical that there is
an answer (or a set of answers).

Thirdly, the question implies that the questioner is at the age of
reflection. Young children do not wonder how to live. And, according to
my account, practical reasoning is an essential part of one’s maturation
from a child to a practically wise human being.

Fourthly, the question calls for a *certain kind of answer*, namely, a
practically reasonable answer. Recall Jay Wallace’s general definition
of practical reasoning as “the general human capacity for resolving,
through reflection, the question of what one is to
do.”[@seppracticalreason] Although sometimes we reflexively act without
thinking, and other times contemplate without acting, (“four and four
makes eight”), it seems obvious, on the face, that deliberation and
resolute action are not like this. One resolves what to do by
considering practical reasons. When a child asks a “how?” question
about, say, how to open a jar, we offer a practical instruction: *hold
the base tightly, grip the lid and twist to the left.* As adults, we ask
“how?” questions about large, multifaceted projects: How to manage a
company merger? How to save for retirement? How to raise a child? The
“instructions” for such answers will be complex. The “how should I
live?” question is simply our most complex long-term project. The answer
or answers cannot be an overly vague resolution (e.g., “help to improve
the world”), nor mere specific platitudes (e.g., “do no harm”). Rather,
a good answer will distinguish between overall good ways and overall bad
ways to live and include a set of practical reasons, some general enough
to give a trajectory to one’s whole life, and others specific enough to
provide guidance through the day-to-day matters of human life.

In short, an answer to the “how should one live?” question requires
practical wisdom. Practical wisdom is unique among virtues in several
ways. First, it is perhaps the one *clearly non-optional* virtue.
Everyone has the obligation to become practically wise, regardless of
circumstances, social roles, aptitudes, cultures, and so on. The
universality of the obligation arises from the mere fact that one is a
practical, rational primate. Secondly, practical wisdom is also unique
in that it enables one to acquire other virtues, such as courage or
moderation, by providing its possessor with the insight and moral skill
to develop specific good habits in the varied circumstances of normal
life. Thirdly, practical wisdom is recursive: the practically wise
person is the most well-equipped to root out folly and become more
practically wise.

The neo-Aristotelian framework for doing ethics views ethical reasoning
as a holistic process that must be sensitive to the whole range of
practical reasons. According to such thinkers, there can be no adequate
theory of ethics without a theory of practical rationality. According to
the arguments of the last chapter, virtues are traits that *enable* one
to live a distinctly human life *and that partly constitute that life*.
In this chapter, I shall argue that the practically wise person is
engaged in “mapping the landscape of value”[@seppracticalreason, section
6] – that is, developing the knowledge and good intentions needed to
pursue what is truly worthwhile and avoid what may seem worthwhile but
is actually worthless. If successful, I shall be lending support to the
age-old view that the skill of engaging in practical reasoning –
reliably and successfully – is the virtue of practical wisdom. The
practically wise person is one who *knows* the answer or answers, if
there are any such answers. The one who answers this question poorly
lives foolishly and, ipso facto, badly. He acts on bad reasons and fails
to act on good reasons. The one who answers it well lives wisely, and
ipso facto, well. Hence, it is essential to virtue that one be
practically wise. Or so I shall argue.

Section 1 breaks ground on this complex matter through a sustained
discussion of John McDowell’s “Virtue and Reason.” I offer a qualified
defense of his thesis that virtue is a form of practical knowledge,
including an initial perceptual sensitivity to the salient facts of a
situation with the skill to do what is required by those facts.

Section 2 highlights an ambiguity in McDowell’s contrast between ‘moral’
and ‘practical’ reasons. He confuses the genus ‘practical reasoning’ for
one species of ‘moral reasoning’ – that is, reasoning about one’s
*obligations to others*. I attempt to remedy this confusion by putting
in historical context the relationship between ‘moral’ and ‘practical’
reasons. McDowell confuses two frameworks for approaching ethics: the
‘quandary frame’ and the ‘character frame.’

Section 3 offers a more coherent alternative. It reprises the argument
that human beings are practical reasoning animals by placing our
distinctive activity in context of the general inclination of all living
things to their own life and health. In this light, practical reasoning
is a necessarily substantive form of reasoning about ends, rather than a
merely instrumental one about means, because in order to have any
reasons at all one must have a first principle of practical reason,
namely, a general evaluative conception of what is to be pursued and
hence how to live.

Section 4 addresses some serious objections to my way of framing ethical
reasoning. For example, how, exactly, is a *rational* calculative
process central to *moral* virtue? Here, I deal with three objections
that challenge the notion that successful practical reasoning is
essential to human virtue.

Virtue as Practical Reasoning
-----------------------------

John McDowell’s “Virtue and Reason” argues, among other things, that
virtue is a particular kind of practical knowledge. Practical reasoning
is both a rational process and also an initial, perceptual sensitivity
that makes visible to us practical reasons. Even though he allows that
practical reasons are ultimately intersubjective features of our social
world, he argues that they are no more and no less objective than
theoretical reasons. In this section, I trace his discussion in some
detail, including his statements of various objections and responses to
them.

What kind of knowledge is virtue, according to McDowell? It is a
practical and dispositional *what to do*. It is not simply
propositional. Rather, it is a non-codifiable perceptual sensitivity to
salient facts along with a disposition that leads the virtuous knower to
act properly – so long as no countervailing psychological factors
interfere. Some objections to his thesis will be addressed as we
proceed.

How does it make sense to conceive of virtue as practical knowledge?
Consider a platitudinous value such as kindness. Suppose kindness is
really a virtue. What does it mean to predicate kindness of someone? We
cannot ascribe a virtue to someone who acts kindly once or twice, or who
does so (even consistently) by pure luck. Justifying the ascription of a
*virtue* requires that a person “has a reliable sensitivity to a certain
sort of requirement which situations impose on behavior” and such
“deliverances of a reliable sensitivity are cases of
knowledge.”[@mcdowell1979virtue 332] McDowell is gesturing toward three
or four plausible criteria for the ascription of a virtue: *reliability*
means the kind person must be *regularly* or *habitually* disposed to
kind thoughts, feelings, and behaviors; *sensitivity* means that the
kind person demonstrates an alertness to the fact that a friend is in
need, a child is sad, an elderly parent is lonely, etc.; *practical
knowledge* means the kind person knows what to do in such situations;
and *intentional behavior* means that the person correctly feels the
imposition to avoid cruel and indifferent behavior and to act on what
the situation requires.

McDowell has made it plausible that sensitivity to reasons to behave a
particular way is at least necessary for virtue. But is it sufficient?
He offers two answers. The first answer is that the presence of a virtue
in someone exhaustively explains her behavior. For example, when the
kind person sees that a situation requires kindness, that “requirement
imposed by the situation” must “exhaust his reason for acting as he
does.”[@mcdowell1979virtue 332] An ulterior interest (say, in a
mercenary reward) would disqualify the action as an example of kindness.
The kind person’s action is explained by the simple fact that it would
be a kind action.

Now, the kindness is not the only reason for action. There are many
reasons for action and many situations where no single overriding reason
is obvious. Rather, the question of what to do seems to generalize into
a question of what is good or advisable, all things considered. McDowell
concedes the point. He illustrates it with the example of a parent who
is overly indulgent to a child out of kindness. Certainly, the parent is
sensitive to what kindness requires but not *sensitive enough* to
fairness or to considerations of the child’s health, and so on.

To accommodate this observation, McDowell generalizes this point to
encompass all of virtue:

> Thus the particular virtues are not a batch of independent
> sensitivities. Rather, we use the concepts of the particular virtues
> to mark similarities and dissimilarities among the manifestations of a
> single sensitivity which is what virtue, in general, is: an ability to
> recognize requirements which situations impose on one’s behavior. It
> is a single complex sensitivity of the sort which we are aiming to
> instill when we aim to inculcate a moral outlook.[@mcdowell1979virtue
> 333]

McDowell is saying that if the kind person’s behavior arises from a
response to the salient facts he is sensitive to, then the virtuous
person’s behavior *in general* is explained by just the fact that it is
virtuous. The virtuous person’s behavior, then, arises from a general
sensitivity to *what situations require.* If virtue is a “single complex
sensitivity” that constitutes an entire “a moral outlook,” then virtue
seems to be not just a perceptual capacity to notice what is required
but also a metacognitive capacity to reflect upon, rank, and order, the
various requirements imposed by a situation before acting accordingly.

I have a complaint about McDowell’s clarification here, which I shall
explain below. In brief, it seems wrong to call the single sensitivity
“virtue” when it includes considerations that do not seem intuitively
moral at all, such as prudential considerations. For now, I must examine
McDowell’s response to the non-cognitivist critic who challenges the
notion that practical reasoning can, by itself, motivate one to action.

Reason, Practice, and Motivation
--------------------------------

The first challenge to his own thesis that McDowell addresses comes from
moral anti-realism, specifically, expressivism. Expressivists are among
the chief contemporary proponents of an alternative, Humean, model of
practical reasoning which denies that practical reason is “a capacity
for reflection about an objective body of normative truths regarding
action.”[@seppracticalreason, section 2. Wallace cites Parfit (2011) and
Scanlon (2014).]

Thus far, it is fairly clear that I have been assuming a kind of
realism. While defending the assumption would take us too far afield, I
should point out that it is not viciously circular. Most of us have no
pre-analytic objection to the seeming fact that some reasons for acting
are good reasons and others bad. Some brute norms (such that it is wrong
to torture animals, or that one is not to use ineffective means to
achieve one’s ends) have a quasi-analytic force to them. Realism about
practical reasons is what Nagel calls a “defeasible
presumption.”[@nagel1989view 143.] Even anti-realism’s most
sophisticated advocates concede the that realism is the default view.
Mackie admits that moral thought and language assumes objectivity, for
the notion of objective value has “a firm basis in ordinary thought, and
even in the meanings of moral terms.”[^53] Gibbard goes so far as to
suggest that Platonism about reasons is *common sense*.[^54]

Nevertheless, anti-realism has a serious challenge to the defeasible
presumption. Subjectivism is motivated by considering a problem about
the status of practical reasons within (a broadly-construed) naturalism.
The anti-realist worries that the “defeasible presumption” lying at the
center of “the main tradition of European moral philosophy” commits one
to non-natural norms and a corresponding non-naturalistic human capacity
to intuit them. Philosophers such as Gibbard insists: “Nothing in a
plausible, naturalistic picture of our place in the universe requires …
non-natural facts and these powers of non-sensory
apprehension.”[@gibbard1992wise 154]

The anti-realist alternatives aim either to debunk the objective purport
of moral reasoning or to reclaim it within the confines of a respectable
naturalism.

The Humean model of practical reasoning asserts that “cognition and
volition are distinct.”[@mcdowell1979virtue 335] Practical reasons
cannot motivate, at least not by themselves.[^55] If this were so, moral
reasoning could not satisfy the “practical requirement” – it could
neither move us to action nor explain *why* we acted. Indeed, a large
part of the appeal of expressivism is that it can satisfy the
*practical* dimension of practical reason (though at the cost of the
*rational* dimension).

Hence, the non-cognitivist critic would be quick to respond to McDowell
with a counterexample of two persons in the same situation who are
sensitive to an identical range of reasons for action but respond
differently. If such a situation were to obtain, it would disconfirm
McDowell’s thesis that virtue is practical knowledge.

The expressivist has a neat explanation of reasoning, action, and
motivation. If reasons cannot motivate by themselves, then practical
reasoners act when reasons co-exist with a conative mental state (such
as a desire, interest, or attraction).[^56] Practical reasoners do not
simply enjoy a “single complex sensitivity” to what situations require.
Instead, the cognitive bit judges an object, while the conative state
provides the movement toward the object. For example, one is aware that
one’s friend is in trouble and that the friend is able to be comforted
(the cognitive bit) and a desire (or motivation or inclination or
settled passion) for helping one’s friend (the non-cognitive bit). The
expressivist would say that surely these two *together* – and neither in
isolation – explains the behavior.

This challenge presents a pair of twin challenges: is virtue-knowledge
*practical* – and if so, wouldn’t it be impossible for an agent to
perceive what a situation requires and still do wrong? Secondly, is
virtue-knowledge *rational* – and if so, mustn’t it be codifiable and
consistent? The very notion of a unitary “practical reasoning” is a
paradox.

### Is Practical Reasoning *Practical*?

McDowell’s response to the expressivist critic is this: one must already
be sensitive to a particular range of requirements for action in order
to even notice the salient facts (e.g., that one’s friend is in
trouble). It is quite plausible to interpret the difference between the
vicious and virtuous person as lying not just in their psychological
reactions to what they notice about the world but *in the noticing
itself.*[See also @little1995seeing] The morally calloused person does
not notice the fact that his actions are causing others pain. Better,
the morally calloused person does not notice the fact *as morally
salient*.

This response from McDowell is not conclusive, but it is a good start.
It highlights, but does not alleviate, the deep disagreement between the
Humean and the Aristotelian camps. He concedes the conditional that *if*
two people are identically sensitive to a morally salient fact but act
differently *then* virtue cannot simply be a sensitivity. But, for
McDowell, one person’s *modus ponens* is another’s *modus tollens.* So
if virtue is to be identified with a single complex sensitivity, then a
supposed situation in which two persons perceive a situation and its
practical requirements identically but act differently cannot
obtain.[@mcdowell1979virtue 333] Is there any way to bridge the divide
without begging the question in either direction? McDowell suggests we
look to Aristotle.

Aristotle allowed that sometimes the “appreciation of what [a virtuous
person] observes is clouded, or unfocused, by the impact of a desire to
do otherwise.”[@mcdowell1979virtue 334] It is possible that a person
correctly perceives what a situation requires (and hence has the
relevant virtue) but fails to act correctly due to interference from
other psychological factors. Desires, fears, etc. might cause a
“distortion in one’s appreciation” of the relevant
reasons.[@mcdowell1979virtue 334]

This Aristotelian reply is also not conclusive. McDowell cites an
objection from Donald Davidson to the effect that a person might fail to
perform the resultant right action *even without such clouded
appreciation.* McDowell concedes. But Davidson’s move changes the
subject slightly, from virtue and vice to continence and incontinence.
For Aristotle, continence (or self-control) is not a virtue. If one can
only do the right thing by gritting one’s teeth and bearing it, one has
not fully attained the relevant virtue. Continence is still
*comparatively better* than incontinence – but not as good as virtue.

The continent person is able to perform the right action because he
recognizes it as right, *despite* countervailing pressures (from
desires, say) to do the wrong action. Since the possession of a full
virtue includes possession of the proper motivation as well, continence
is only needed in the absence of a fully developed virtue. Put
differently, the virtuous person is not just one who “balances” reasons
to φ against countervailing reasons to π. The virtuous person is the one
for whom simply identifying the appropriate reasons to act silences
countervailing reasons. For example, *in this situation, courage
requires that I run into danger.* The virtuous persons acknowledges the
danger (and feels rightly apprehensive) but also sees that courageous
action in the face of this danger is required; the latter perception,
according to McDowell, “silences” other pressures.[@mcdowell1979virtue
335] The merely continent person has to “weigh” reasons; the virtuous
person fluently *acts* on the best reason.

In my view, McDowell’s reply to Davidson’s objection is not quite
adequate. Fully explaining the common occurrence that we judge what is
to be done but fail to do it would require a lengthier discussion. I
have argued in chapter 4 that some virtues are excellent rational
*practices*. Following Aristotle, I would suggest that the fullness of
virtue is not merely the sensitivity to what is required – which an
incontinent person might have – but also a well-ordered psychology
(including emotions) and a set of rational habits that empower the agent
to follow through on doing what is required. Virtues require habits, not
just knowledge.

We can contrast virtue with continence/incontinence in this way: Unlike
the continent person, the virtuous agent has overcome the psychological
factors or other factors that cloud the appreciation of what is
required. And unlike the incontinent person, the virtuous agent has
cleared away other factors that interrupt the execution of the thing to
do. Once the fullness of a virtue is attained, the possessor does not
need to stop and “weigh;” but sees what is required and acts. (I shall
comment a bit more on moral motivation below.)

### Is Practical Reasoning *Rational*?

McDowell’s case that practical knowledge can motivate the virtuous
person requires addressing twin challenges. We have addressed one side
of the paradox which challenges the practicality of virtue-knowledge.
The other side of the paradox challenged its *rational* credentials.
Pretty clearly, the paradigmatic case of knowledge is theoretical
knowledge, i.e., *knowledge that p*. Such knowledge is categorical,
propositional, and codifiable into a deductive logical system.
McDowell’s critic then poses the following argument: knowledge is
codifiable. However, virtue-knowledge is practical knowledge or
‘knowing-what-to-do’, which is not codifiable. Therefore, virtue must
not be knowledge.

The error in this objection, McDowell thinks, is not an error in moral
theory but a “deep-rooted prejudice” that rationality is a
rule-following procedure. If rationality is a rule-following procedure,
then it follows that *either* practical rationality and morality are
likewise rule-following procedures *or* that practical rationality and
morality are not, ultimately, sufficiently *rational*. Some Humean
philosophers (but not necessarily Hume) think that morality is a
non-rational domain of sentiments, desires, commitments, approvals, and
so on. Other Kantian philosophers (but not necessarily Kant) think that
morality is a rational domain and hence must be a matter of identifying
first principles and applying them to particular situations. What both
parties share is a belief that “rationality must be explicable in terms
of being guided by a formulable universal
principle.”[@mcdowell1979virtue 337. MacIntyre, similarly, denies the
assumption that normative ethical rules can be derived from universal
ethical principles the way we “apply” universal logical truths to
particular logical conclusions via a middle term. Cf.
@macintyre1984does] This common belief McDowell wishes to refute.

McDowell’s argument here (drawing on Wittgenstein and
Kripke[@kripke1982wittgenstein]) is that even apparently obvious cases
where the rational thing to do seems to require following an objective
rule turn out to be cases of a much messier process in which there is no
such objective rule we can appeal to. For example, take the objective
rule of extending a series of numbers two at a time. Suppose Smith
instructs Jones to “add 2” to a number and continue applying the rule
indefinitely. We are confident (as is Smith) that Jones will “churn out
the appropriate behavior with the sort of reliability which a physical
mechanism, say a piece of clockwork, might have.” We tend to expect that
Jones will produce “2, 4, 6, 8,” etc. McDowell thinks this confidence is
based on postulating a “psychological mechanism, underlying his
behavior, by an inference analogous to that whereby one might
hypothesize a physical structure underlying the observable motions of
some inanimate object.”[@mcdowell1979virtue 337] The postulate of a
psychological mechanism is mistaken because, as it turns, out, the rule
being followed is not so simple as “add 2 indefinitely.” It is logically
possible that Jones interpreted Smith’s instruction as a different rule
that happened to produce the same result. The attempt to stamp out this
possibility by adding new meta-rules or sub-rules iterates the problem.
It is still logically possible that Jones follows a *different*
meta-rule or sub-rule that happens to produce the same result.
Wittgenstein’s conclusion is that even apparently simple rules,
successfully followed, cannot be exhaustively described.

McDowell’s conclusion is that the true “ground and nature of our
confidence” is our participation with Jones in a common form of life.
What is a ‘form of life?’ This is a term of art, also drawn from
Wittgenstein and quoted with approval from Stanley Cavell. It refers to
the shared result of acculturation or formation. For example, how do we
learn reliably to use words and expressions in our native language?
There is no clear mechanistic process that explains exactly when a child
learns to make exclamations – such as a pained “ow!” or an excited
“ooh!”. There is no clear mechanistic process by which we learn when to
laugh at jokes or when to cry in pity. Instead of a mechanistic process,
McDowell suggests that children learn words and behaviors by “bildung”
or formation. The result is a “congruence of
subjectivities.”[@mcdowell1979virtue 339] Jones is able to follow
Smith’s rule (and we are confident that we know what his instruction
meant) even though it is not stated exhaustively because we all share a
common practice of, say, adding or producing a series of numbers. More
generally, all of our shared rationality is not grounded in “external”
objective rules but in a shared form of life.

It is disconcerting to many to consider that nothing keeps rationality
“on the rails” but a congruence of subjectivities. McDowell admits this
is a disconcerting hypothesis; it induces “vertigo.” But, he says, our
response to such vertigo should not be to embrace a “consoling myth”.
That “consoling myth” consists of two notions: (a) that rational
rule-following is enabled by a psychological mechanism that guarantees
consistency; and (b) that there exist objective facts of the matter over
and above the congruence of subjectivities. If we abandon these two
notions and embrace the model of deductive rationality as grounded only
in our intersubjective form of life, then the corresponding model of
practical rationality will become tenable.

I think McDowell concedes too much here, as I shall explain below.
Nevertheless, my purpose here is to agree with McDowell that both forms
of rationality – the practical and the theoretical – are on a par. They
stand or fall together. Either they are both intersubjective or both
objective. Practical reasoning may be relatively less codifiable than
theoretical reasoning, but each is equally a form of knowledge.

McDowell asks a related query: what, if anything, guarantees that the
moral person’s behavior is intelligibly the same from case to case? If
moral knowledge were formulable as a universal principle, then it would
be consistent from case to case and situation to situation; but if, as
McDowell has been arguing, both deductive reasoning and practical
reasoning are not merely rule-following mechanisms, then how do we
explain the virtuous person’s reliably correct behavior? His answer
invokes Aristotle’s notion of a practical syllogism. According to
McDowell, the ‘practical syllogism’ takes the following shape:

1.  X is good to do, desirable, worthwhile, etc. (E.g., it is good to
    instantiate justice in the classroom).
2.  Z would be X. (E.g., giving everyone a chance to re-take a quiz that
    was unavailable due to technical problems would instantiate justice
    in my classroom.)
3.  Therefore, Z would be good to do, desirable, worthwhile, etc.

On the strictly deductive logical model, the role of the major premise
is to provide solid universal ethical principles from which it is
possible to derive a codified set of particular moral duties. McDowell
resists this model. The strictly non-cognitivist alternative is that
there must be no universal ethical principles at all – only universal
psychological states, such as consistent desires, plans, values, or
norms. McDowell also resists this model. Instead, the role of the major
premise is to articulate a “certain conception of how to live… [namely]
the *virtuous person’s conception* of the sort of life a human being
should lead.”[@mcdowell1979virtue 343. Emphasis added.] What kind of
life should a human being lead? The answer “cannot be definitively
written down.”[@mcdowell1979virtue 343]

If the kind of conception of a good life that the virtuous person has is
approximate and non-codifiable, it becomes hard to see why we are
bothering to fit moral reasoning into a syllogistic pattern at all.
McDowell’s response is that understanding virtue-knowledge within a
practical syllogism *does* a good job of providing a plausible
explanation of moral motivation (reasons one might act in some way) and
moral behavior (reasons one acted that way). To paraphrase McDowell:
“Explanations of judgments about what to do are also explanations of
actions.”[@mcdowell1979virtue 342. Verbatim: “The explanations, so far
treated as explanations of judgments about what to do, are equally
explanations of actions.”] I can explain your behavior by understanding
that you were concerned for your friend’s welfare and so offered to
help. Likewise, you can explain your decision to help simply by citing
the fact that your friend was in need. So the general structure of the
practical syllogism is useful.

What’s more, McDowell concedes that there is a kind of circularity to
his account: “the rationality of virtue… is not demonstrable from an
external standpoint.”[@mcdowell1979virtue 346.] And: “Any attempt to
capture it in words will recapitulate the character of the teaching
whereby it might be instilled: generalizations will be approximate at
best…”[@mcdowell1979virtue 343] The virtuous person’s conception of how
to live is itself conditioned by the moral outlook. That conception of
how to live, in turn, conditions what particular saliences are noticed
(what minor premises) and generates practical conclusions about what is
to be done. The upshot of the combination of non-codifiability with a
practical syllogistic form is that the virtuous person takes for a rule
of life some conception of how to live but that this conception is part
of what it means to be a virtuous person – and thus ensues a certain
circularity.

McDowell bites the bullet on the incorrigible intersubjectivity of
theoretical and practical reasoning. I think he does so because he fails
to grasp Foot’s insight that objective, natural, normative facts are
able to “keep us on the rails.” I am not motivated to think this out of
a desire to be “consoled.” In any case, the presence or absence of a
frightening vertigo in the arguer is irrelevant to the argument. The
notion that all practical and deductive reasoning is ultimately
answerable to the world is a more adequate explanation. As I have argued
in chapter 2, both scientific reasoning and ethical reasoning can
conform or fail to conform to the relevant range of normative facts. I
shall criticize McDowell’s intersubjective notion a bit more in the next
chapter.

In sum, McDowell thinks virtue is a kind of practical knowledge. That
is, virtue is a sensitivity to salient facts that call for a particular
response and that intrinsically motivates the virtuous person that
response – absent interfering passions. The hypothetical counterexample
presented by his Humean critic is one wherein two agents are “sensitive
to” or “notice” identical reasons for action but do not act identically.
McDowell’s response is that while noticing a requirement for action is
necessarily motivating *to some extent*, other psychological factors may
interfere with the resulting correct action. Furthermore, the kind of
“knowledge” that virtue amounts to is uncodifiable, but that does no
harm to the account. Virtue-knowledge is rather a broad conception of
how to live and a series of specific sensitivities to a range of
specific practical reasons. Practical reasoning is *consistent*,
moreover, but not by being “objective” (in the sense that even McDowell
admits would be desirable) but by being rooted in our communal form of
life – precisely the same way in which logical reasoning is. Both are
“intersubjective” and rooted in our form of life, but both are as
objective as need be.

### Moral and Practical Reasoning

While I shall discuss what I think McDowell gets wrong below, on my
view, he gets this much right: practical reasoning is indeed by
definition a form of *reasoning*. It is like theoretical reasoning in
that it is normative.

Broadly, we can say that theoretical reasoning is a process by which I
aim to determine *what to believe* – to answer the question “What should
I believe?” When I assess evidence for and against some proposition p, I
am looking for *reasons* to believe p is true or false. The successful
conclusion of a rational argument is the judgment that p or not-p. (Or I
may not have enough evidence to judge either way, in which case I may
withhold judgment.) Similarly, when I consider a scientific hypothesis,
I suppose that p and then conduct an experiment that will reveal reasons
that confirm or disconfirm the supposition. To fail to believe p upon
coming to know good evidence for it, or to believe p in spite of good
evidence against it, is to make an intellectual error. If q entails p
and I already know and affirm that q, then I *ought* to affirm that p.
Similarly, if some reason to π entails a decisive reason to φ, and I
already know and am committed to π, then I ought to φ.

So far as we know, all theoretical reasoners are also practical
reasoners. We can imagine creatures such as angels, Artificial
Intelligences, and intelligent aliens who might think without acting;
but so far as we know, to be a reasoner at all is to be responsive to
what Sellars called the “space of reasons,” including both practical and
theoretical reasons. This consideration is part of the reason why, in
chapter 3, I insisted that practical reasoning, and *not* abstract
theoretical reasoning, defines human nature. If this is right, then the
burden of proof lies with those who would artificially separate the
*knowing* and the *practicing*.

That said, my complaint against McDowell’s account is that he confuses
moral and practical reasons. Suppose Jane can pretty well diagnose a car
engine by listening to the way it whines, hums, and clicks. When all
John hears is noise, Jane is “sensitive to a range of requirements for
action” and knows what to do (say it needs a new timing belt). By
McDowell’s lights, she has a practical disposition which is virtue. It
strains common sense to call any and all such sensitivities “virtues.”

Even if we introduce a requirement that practical knowledge must be
concerned with requirements pertaining to other people, similar
analogies arise in other contexts. For example, an American football
kicker is sensitive to the salient facts of what is required to score a
field goal, which will help his team to win. And a general contractor is
sensitive to the salient facts of what is required to build a structure
up to code, and so on, which will help protect the safety of whoever
ends up living in the structure. Both of these practical skills *help
others* but neither seems to amount to moral virtue. Even though a
contractor willfully who fails to build a structure safely might be
morally and legally liable for any subsequent injuries, something
strikes us as odd about classifying the skill as a virtue.

There is a second, related complaint. McDowell admits that one might
potentially need to rank, order, and weigh a dozen different kinds of
reasons (kindness, fairness, appropriateness, prudence, etc.) before one
resolved what to do. He seems to switch from talking about moral reasons
to talking about *any* practical reason without any mention of the
switch. By failing to render a clear distinction between moral and other
practical reasons, I believe McDowell falls prey to a habitual way of
framing moral discussions that is a subtle mistake.

The habitual way of framing moral discussions we may call the “quandary
frame,” borrowing the term from a classic article by Edmund Pincoff.
Pincoff contrasts “quandary ethics” with another way of framing ethical
discussions which he calls “character” ethics. On this frame, ‘moral’
considerations contrast with prudence and any other kind of practical
consideration. ‘Moral’ considerations most commonly refer to
“other-regarding” considerations (opposed to self-regarding ones),
altruistic (as opposed to egoistic), considerations of benevolence (as
opposed to selfishness), or conscience (as opposed to self-love).[^57]

The contrast between moral and all other practical reasons gives rise to
a distinctive way of approaching ethics. Pincoff writes of quandary
ethics:

> The business of ethics is to clarify and solve “problems,”
> i.e. situations in which it is difficult to know what one should do;
> that the ultimate beneficiary of ethical analysis is the person who,
> in one of these situations, seeks rational ground for the decision he
> must make; that ethics is therefore primarily concerned to find such
> grounds, often conceived of as moral rules and the principles from
> which they can be derived; and that meta-ethics consists in the
> analysis of the terms, claims, and arguments which come into play in
> moral disputation, deliberation, and justification in problematic
> contexts.[^58]

According to Philippa Foot, the quandary frame is the way most modern
philosophers approach ethics. She says:

> Many if not most moral philosophers in modern times see their subject
> as having to do exclusively with relations between individuals or
> between an individual and society, and so with such things as
> obligations, duties, and charitable acts… ‘moral’ and ‘prudential’
> considerations [are] contrasted in a way that was alien to Plato or
> Aristotle.[@foot2001natural 68]

Relatedly, Martha Nussbaum says:

> This question [of how ‘moral’ ends figure among other ends] is posed
> in a characteristically modern way, presupposing a distinction between
> the moral and the non-moral that is not drawn, as such, by the Greek
> thinkers. But if one objects to that characterization, one can
> rephrase it: for example, What role does concern for others for their
> own sake play in here scheme of ends? What role does political justice
> play in her scheme of ends? And so forth.”[@nussbaum1999virtue 174]

Kant and Hume agree on the quandary frame, despite their significant
substantive disagreements. They both present morality as a kind of
crisis strategy. On any given normal day, agents are free to pursue
their own self-interested inclinations – get a good job, save for
retirement, eat healthy foods, exercise, make friends, and so on – so
long as they commit no wrong. So long as life presents no moral
dilemmas, moral reasoning is idle.

The alternative type of ethics is what Pincoff calls “character” ethics
(of which I take neo-Aristotelian virtue ethics to be a token). Such
ethics is focused on the long-term project of living well by executing
worthwhile goals in every day life. Aristotle is the premier example of
a character ethicist because he thought of ethics as a branch of the
whole practical enterprise:

> …[ethics and politics] is a very wide-ranging subject having to do
> generally with the planning of human life so that it could be lived as
> well as possible. Moral problems are given their due but are by no
> means stage-centre. The question is not so much how we should resolve
> perplexities as how we should live.[@pincoffs1971quandary 553-4]

The Greek way of framing moral questions viewed *all* practical ends as
‘moral.’ MacIntyre provides the clearest summary of the older use of
‘moral’:

> ‘Moral’ is the etymological descendant of ‘moralis’. But ‘moralis’,
> like its Greek predecessor *ethikos* – Cicero invented ‘moralis’ to
> translate the Greek word in the *De Fato* – means ‘pertaining to
> character’ where a man’s character is nothing other than his set
> dispositions to behave systematically in one way rather than another,
> to lead on particular kind of life… The early uses of ‘moral’ did not
> contrast with ‘prudential’ or ‘self interested’” nor with ‘legal or
> ‘religious’… The word to which it is closest in meaning is perhaps
> most simply ‘practical.’[@macintyre1984after 38]

MacIntyre’s point is not merely etymological; it is conceptual. When
quandary ethicists conceive of ‘moral reasons’ as a special overriding
type of practical reason concerned with duties to others (contrasted
with self-regarding prudential reasons), they fall under the illusion
that moral reasons may not be practical and that practical reasons may
not be moral. By contrast, the character ethicist views life as
presenting the variety of possible ends that could clash or harmonize
that all need to be accounted for.

It is helpful to observe that, at some point in the history of western
moral philosophy, the topic of the “moral” began to separate off from
the broader topic of the practical. Foot cites Mill as an early
proponent of the distinction:

> J. S. Mill, for instance, expresses this modern point of view quite
> explicitly, saying in his essay *On Liberty* that ‘A person who shows
> rashness, obstinacy, self-conceit . . . who cannot restrain himself
> from harmful indulgences’ shows faults (Mill calls them
> ‘self-regarding faults’) which ‘are not properly immoralities’ and
> while they ‘may be proofs of any amount of folly . . . are only a
> subject of moral reprobation when they involve a breach of duty to
> others, for whose sake the individual is bound to have care for
> himself.’[@foot2001natural 68]

Mill distinguishes folly from immorality by treating folly as a failure
to provide goods for oneself. He treats imprudence as “bad” but not
*morally bad.*

While I don’t intend to suggest that there is something automatically
laudable about the older Aristotelian emphasis, my contention is that
the modern emphasis on “relations between individuals or between an
individual and society” fails to capture much of what is interesting
about the “how should one live?” question. The modern distinction
obscures the real ethical situation.

To return to McDowell, I can now put my complaint in clearer relief: is
he a quandary ethicist or character ethicist? In my view, McDowell’s
view represents a mixture (indeed, a confusion) of the two. Like the
character ethicist, he emphasizes the “how should I live?” question and
invokes practical knowledge as an important part of the answer. However,
like the quandary ethicist, he represents moral considerations
pertaining to the rights, obligations, or duties to others (such as
kindness) as a special, perhaps overriding, kind of reason. He does not
seem to notice that broadening the virtuous person’s perceptual
sensitivity to what *any* situation requires renders his account
ambiguous. Are moral reasons *one type* of practical reason, or can any
practical reason count as a “moral” reason (broadly construed).[^59]

Practical Reasoning as Pursuing the Human Good
----------------------------------------------

The remedy for this confusion is to return to and defend a more
consistent account of practical reasons. Happily, this account will
reinforce what we have argued above about the natural normativity in the
human life form and all organic life. This section builds on the work of
Philippa Foot and on Jennifer Frey’s recent discussions of Anscombe and
Aquinas.[^60]

On the Aristotelian account, as developed by Aquinas, practical
reasoning is by definition an end-oriented activity that aims at the
perceived good of one’s form of life. The primary question is not “why
should one respond to moral reasons instead of prudential ones?” but
“why do we act at all?” and “how can we act well?” Asking this question,
and answering it, is a practically rational activity that defines the
human life form. Certainly, as Foot says, some practical reasons have to
do with “obligations, duties, and charitable acts” to others; but others
pertain to what is required for oneself and even for third-person
objects such as the environment, possessions, and perhaps even abstract
objects.

Considered thus broadly, the normativity of practical reasoning is
clear: some reasons for acting are good while others are bad. Errors of
morality, then, belong to a wider class of practical errors. As Foot
says: “I want to show that judgments usually considered to be the
special subject of moral philosophy should really be seen as belonging
to a wider class of evaluations of conduct with which they share a
common conceptual structure.”[@foot2001natural 66-67] On this frame, any
reason to φ or not to φ is a practical reason, and successfully sorting
through all such reasons is a virtue, namely practical wisdom.
Unsuccessfully doing so is the vice of imprudence or practical folly,
which inhibits one’s ability to live a human life.

Defending the Aristotelian account requires us to revisit in more detail
some of what was argued above in chapter 2. Recall the observation that
all organisms act toward ends, with or without reflection. Frey
summarizes Aquinas in this way:

> All living things are a self-sustaining system of powers that
> functions to bring the living thing into being and to sustain its
> being. The movement of any part of a living thing, at any particular
> moment, is necessarily explained by reference to the movement of the
> whole thing towards a single end: the coming to be, maintenance, or
> reproduction of that very form of life.[@frey 68]

As I argued above, all living things exhibit teleological movement. In
proper circumstances, they grow into maturity, which is the
exemplification of their form of life. This form of life is what Aquinas
calls a thing’s “nature”: wolf hunts in packs by nature, trees extend
roots into the ground by nature, reptiles warm themselves in the sun by
nature, and so on.

The sunflower has no consciousness with which to incline toward
sunlight. ‘Things are specified by their power.’ When it comes to higher
organisms, insects and mammals and so on, organisms have “appetite.”
They demonstrate the capacity to sense and to move consciously toward or
away from certain objects: The antelope pursues healthy grass and flees
a lion. The animal can only experience what is good or bad for it as a
particular object.

While natural norms are features of all living beings, human beings are
distinct in also being aware of such norms. Humans grow, reproduce, and
enjoy conscious experiences like other animals and also *know* that they
do so. Obviously, plants and animals do not “naturally incline” toward
their good by reflecting or choosing it. Frey points out:

> Aquinas would agree with us that it is a category mistake to say that
> a sunflower wants to grow towards the light, if by this we mean that
> the flower somehow registers a positive feeling or has an inner
> impression towards the light, which “causes” it to move toward the
> light. The plant does not apprehend or desire anything; thus Aquinas
> is very careful to say that it does not have a power of appetite. In
> fact, Aquinas is at pains to note that a plant has no window onto the
> world at all – it just has conditions in which it characteristically
> comes into being, maintains, and reproduces itself.[@frey 69-70]

Lower organisms naturally incline toward their own good. Higher
organisms perceive objects but do not perceive them *as* falling under
universal categories. By contrast, a human being can recognize
universals. Human beings are specified by their “power” – their capacity
to engage in cognitive and deliberative activities. While animals can
not only sense but *perceive*, humans have the capacity of
“intellection” – the power of abstracting formal properties from what is
perceived. An animal can *sense* an informed, organized object; an
animal can be affected by the object. But the human animal can *acquire
information* from the organized object. Animals may perceive something
*as* dangerous or *as* desirable. Human beings perceive *that* the
dangerous thing is a predator or the desirable thing *is
food*.[@haldane1996coming]

The extra ability to perceive under universal categories brings with it
the human capacity for taking up natural inclinations or aversions in a
deliberative act. Natural inclinations may be underwritten or
overridden. Confronted with a delicious and healthy salad sitting on
someone else’s plate, I recognize it *as not mine* and hence choose not
to reach for it. Confronted with a lion in a zoo, I choose not to flee,
for I recognize it *as not dangerous*. Frey summarizes:

> Rational animals, like any animal, have a natural inclination towards
> their good as a whole, and like lower animals this power is actualized
> through their apprehension of things in the world. But Aquinas argues
> that a rational animal relates to the world through the application of
> universal concepts, and thus it is inclined to pursue or avoid things
> under an intellectual, universal apprehension of them. Thus, Aquinas
> says that the will is inclined towards its objects under the formality
> of the “universal good,” rather than the particular good.[@frey 75]

By the same token, human beings are capable of an extra ability to err.
The conclusion that all living things move toward their own natural ends
is compatible with the biological judgment that some specimens are
defective, just as it is compatible with the ethical judgment that some
agents – such as Dostoevsky’s Underground Man – are practically
irrational in failing to pursue their own natural ends. Human beings are
supposed to practically reason well. When they do not, the defect that
arises is more than merely animal. Any animals might be afflicted by
sickness or injury; only human animals can inflict themselves with new
injuries and even new illnesses.

We have been speaking of the human capacity for recognizing and pursuing
particular ends as good. As we saw in chapter 4, a full conception of
virtue demands that we expand our scope to include the whole of life,
the conception of our human good that constitutes the answer to the “how
to live?” question. McDowell gets this part right in his discussion of
the practical syllogism. Every rational practice is undertaken in
pursuit of some particular end *in context* of a total conception of
what is good in general. Frey continues:

> Consequently, we can say that rational animals have an understanding
> of different levels of ends, and at least a vague sense of how they
> are supposed to hang together as a whole. This conception of how it
> all hangs together is what Aquinas calls the ultimate end – a rational
> animal’s general, conceptual understanding of how to live or go on.
> Aquinas thinks that any sane, mature adult will necessarily have
> cobbled together some such conception. Aquinas calls this conception
> “the universal good”, and he argues that it is the will’s proper
> object. Everything that is willed is willed under this rational aspect
> of good, as to be pursued because *in accord with my general
> conception of the good.* In fact, Aquinas thinks there could be no
> reasons unless a rational animal has a general conception of its own
> good, and thus a general sense of how to live.[@frey 78-9, italics in
> original.]

Frey’s argument here is that the question of ‘how to live’ is a question
about my good as a human being; answering that question requires the
human activity of practically reasoning. And since every “sane, mature
adult” engages in this activity, every sane mature adult has a general
notion about the answer. The crucial insight is that without such a
general notion, we *would not engage in rational action at all*. Frey
continues:

> No human action is intelligible without attributing to the agent
> herself some conception of this end, no matter how inarticulate,
> unsystematic, or unreflective it might be. Aquinas takes it for
> granted that in coming to be a human being – i.e., being raised in a
> community of other human beings, coming into the possession of
> concepts, a language, and coming to have a world – one comes into some
> such conception, and thus comes to act voluntarily.[@frey 87]

Human beings act. And all intelligible actions are undertaken in pursuit
of some end. Therefore, all intelligible actions of humans are
undertaken in pursuit of some end. This conclusion can accommodate the
commonsense observation that not *every* move we make counts as an
intelligible action. Aquinas makes a helpful distinction between the
“actions of a human” and “human actions.” An *action of a human* can be
any motion of a human body: mumbling while asleep, scratching an itch,
or idly tapping a foot. A *human action* is by definition an action in
pursuit of a goal which is perceived as a good. A human action is an
action such as running a race, starting a conversation, or tapping out a
message in Morse Code. These actions are both intelligible and
intentional in a way other animal actions are not. With this distinction
in mind, we can state an important clarification. It is not the case
that a human being without *any* practical reasons would perform immoral
deeds; a human being without *any* practical reason would not do
anything at all. He might move about, driven by instinct or fear or
desire, but such a person would not engage in any human actions. Like
Melville’s Bartleby the Scrivener (from the short story of that title),
the person who does not engage in practical reasoning or identify any
practical reasons would simply waste away and
die.[@melville1966bartleby]

Aquinas’ distinction between human actions and the actions of a human
can also go to explain some compulsive or addictive behaviors.
Unfortunate people in the overwhelming grip of, say, a heroine
addiction, might be injecting themselves with the drug against their own
evaluations of what should be done. However, in extreme cases of
addiction, the action hardly falls under the description of a human
action. Heroine is so highly addictive that one or two uses can create a
dependency that lasts a lifetime. The addict’s initial decision to use
the drug can still fall under the description of a human action, perhaps
aimed at some perceived good such as pleasure or joining in a social
group. But just as one is free to choose to slide into a muddy hole in
the ground but not necessarily free to climb back out, one is free to
use a habit-forming drug but not necessarily free to stop feeling the
overwhelming compulsion, even though one might wish never to use again.

If all action aims at some good, then where does the process begin? How
can one pursue ends *before* actualizing the natural ability to
practically reason? We can again compare practical reasoning with
demonstrative or theoretical reasoning. Aquinas puts the comparison this
way:

> …as “being” is the first thing that falls under the apprehension
> simply, so “good” is the first thing that falls under the apprehension
> of the practical reason, which is directed to action: since every
> agent acts for an end under the aspect of good. Consequently the first
> principle of practical reason is one founded on the notion of good,
> viz. that “good is that which all things seek after.” Hence this is
> the first precept of practical reason, that “good is to be done and
> pursued, and evil is to be avoided.[@aquinas IIa. Q.94. Art. 2]

Aquinas points out that the first thing human beings apprehend as
theoretical reasoners is simply “existence” or “being” – infants
perceive that some things are there and others not there. They
eventually come to perceive objects *as* objects, as individual objects,
and to name and categorize them with language acquired in a social
setting. Likewise, the first thing human beings apprehend as practical
reasoners is simply the “good” or “desirable.” The use of ‘good’ here,
it bears repeating, is not a special moral sense of good, but simply
means ‘desirable’ or ‘to be pursued.’ An entity is ‘good’ when it is
considered as an object of inclination. Hence, infants perceive that
some things are to be pursued and others avoided. To be *theoretically*
rational is to judge a proposition p as true or false, as best one can,
according to the rational assessment of the reasons for affirming or
denying p. Similarly, to be *practically* rational is to judge a
practical reason φ to be pursued or avoided, in accord with the rational
assessment of the reasons for pursuing or avoiding φ. Without a general
principle in either case, practical reasoning and rational practice are
unintelligible.

Given this basic and abstract formulation of the structure of practical
reasoning, we can further specify good ends. Just as the basic structure
of reasoning begins with the apprehension of being in general and grows
to include apprehension of particular beings, concepts, and categories,
practical reason begins with the apprehension of good in general and
then determines particular goods.

> Practical reason is the movement of thought towards, rather than away
> from, material particulars…. practical reasoning is a movement from
> general knowledge of what is good and how to live, towards the
> production of the kind of life that is essentially characterized by
> such knowledge. When it is done well, what is understood is the same
> as what is produced: human form or human life.[@frey 2]

Such basic goods are apprehended as contributing to a distinctively
human life form.

> For practical reason, the starting points are the most primitive human
> goods that the will is naturally inclined to seek: life, knowledge,
> family, friendship, play, political community, and so on. These are
> the ends that all human beings want for their own sake, as
> intrinsically valuable to them. And they want these things in a
> rational way – viz., because they have a conceptual apprehension that
> they are constitutive of their general good.[@frey 88]

Having said this, we should make two clarifications. First, I think Frey
is asserting a generic truth when she says “these are the ends that all
human beings want”; the truth admits of exceptions. Whatever the causes
of psychopathy, some people seem insensitive to the obvious draw of
natural ends. Such people don’t want knowledge, don’t care to have
friends, don’t like to play, detach from their families, and in some
cases show careless disregard for life – both their own and that of
others. The important point is not that “primitive human goods” are
pursued by all without exception – though indeed they are pursued by the
vast statistical majority. The important point is that without some
notion of primitive human goods, we could not identify disorders like
psychopathy. Social behavior is not merely statistically normal but
normative.

Secondly, some readers might object that this account equates “pursuing
the good” with “pursuing the human good,” including such “primitive
goods” as life, knowledge, friendship, and so on. Might there be goods
that are *good simpliciter* that one ought to pursue, *regardless* of
their bearing any internal relation to the human life form? Iris Murdoch
argues along these lines that the starting point of ethical training
must be aesthetic training.[@murdoch1998sovereignty 90] One must
cultivate the ability to see intrinsic value by first learning to see
intrinsic beauty in art and nature, learning to appreciate it
dispassionately. Just as the dispassionate pursuit of knowledge aims at
knowledge of external realities (physical objects, animals, chemicals)
and not just at knowledge of knowers, might not the pursuit of the good
aim at external goods?

McDowell takes Murdoch’s thesis in a different direction. He argues that
“the remoteness of the Form of the Good is a metaphorical version of the
thesis that value is not in the world… The point of the metaphor is the
colossal difficulty of attaining a capacity to cope clear-sightedly with
the ethical reality which is part of our world.”[@mcdowell1979virtue
347] For McDowell, this recognition of the difficulty of ethical
training can benefit one “negatively, by inducing humility, and
positively, by an inspiring effect akin to that of a religious
conversion.” For McDowell, then, ethical (and aesthetic) training is not
progress toward the *discovery* of objective value but toward the
unfolding of one’s subjective or intersubjective values.

I am content to remain neutral with respect to these two options.
*Minimally*, practical reasoning is the ability to judge the good of the
human life form. This minimal ability is compatible with the paradoxical
thought that what is good for humans is not *merely* the human good.
What is good for humans might be the good simpliciter. It is needful,
before examining this further issue, to defend the notion of basic,
human goods. That is my aim here. Jennifer Frey summarizes:

> …all practical reasoning is ultimately reasoning for the sake of
> attaining or maintaining these ends [i.e, basic human goods].
> Consequently, all practical reasoning is ultimately for the sake of
> living the sort of life that pertains to man. Indeed for Aquinas,
> there could be no practical teleology without natural teleology, since
> there would be nothing to reason towards if the will were not by
> nature inclined towards the exemplification of human form.[@frey 66]

To sum up the account thus far, all organisms incline toward the good of
their life form, including those basic goods that enable the full
actualization thereof. Various organisms express this inclination in
various ways. For lower organisms, consciousness plays no part in this
process; for higher organisms, consciousness does play a part. For
humans, the essential difference is a sensitivity to the space of
reasons, both evidential and practical. ‘Practical reasoning’ is the
name for the whole complex process of perceiving certain salient facts
as reasons to pursue or avoid some course of action, and comparing and
ranking competing reasons in light of an overall conception of a good
human life and acting accordingly. None of this is intended to deny that
evaluative practical reasoning arises in a normal process of
socialization. Rather, that our conception of how to live would arise
that way is what we would predict for rational primates who speak and
live in society.

Objections
----------

I am now in a position to state and respond to three objections.

**1. Procedural Reasoning**: One challenge is the familiar notion that
practical reasoning is a value-neutral procedure by which we line up
means to our ends.[^61] On this view, moral reasoning is about the
morally good and bad while practical reasoning is about something else
entirely, such as the prudent or imprudent, the advisable or
ill-advised. So how could an *intellectual* exercise be essential to
*moral* virtue?

**2. Reason, Practice, and Motivation**: Another challenge comes from
non-cognitivism (especially expressivism).[^62] The worry is that
practical reasons by themselves can’t motivate us to act (without
complementary psychological attitudes such as desires), while
motivations to act cannot be rationally evaluated as true or false. Is
practical reasoning really *rational*? And if so, is it really
*practical*? It seems that it must be either one or the other.

**3. Overriding Reasons**: A third challenge is a familiar distinction
between “moral reasons” on the one hand and “prudential reasons” on the
other, where moral reasons are overriding reasons. On this distinction,
one can be *foolish* by failing to act on some considerations, but one
is immoral by failing to act on relevant overriding moral reasons. If
practical reasoning is a process of identifying or inventing what is
advisable or ill-advised (but not ultimately binding), then how does
this process relate to an appropriate sensitivity to what is morally
permissible or impermissible (which is ultimately binding)?

### On Procedural Reasoning

According to the **Procedural Reasoning** objection, reasoning is not
about ends but only about means. Practical reasoning is a procedural or
instrumental process. The critic alleges that one may only criticize
Smith as “irrational” when Smith fails to use the necessary means to her
own ends, but one may not criticize Smith’s *ends themselves* as
irrational. For example, if we define practical reasoning as the process
by which one adjudicates the means to *one’s own health*, then *any*
unhealthy action (e.g., eating delicious but less-than-healthy food)
would be ipso facto irrational. Isn’t it problematic to build into the
definition of rationality any specific, ready-made ends?

The first response to this challenge is that, even on the procedural
view, practical reasoning *must necessarily have a certain intelligible
structure*. The advocate of the procedural view, no less than the
advocate of the substantive view, needs a sufficiently general starting
point for procedural reasoning to even get off the ground. Frey’s
candidate for that starting point is the maximally general conception
that “good is to be done and evil avoided” or that “one must pursue
one’s own good.” Her argument concluded that when practical reasoners
act at all, they act *by definition* in pursuit of a particular object
falling under a universal category. In order to construct *any*
practical syllogisms as we do, one needs a sufficiently broad “major
premise.”

A second response to Frey’s view is that it does not build in very
*specific* ends. The built-in end is quite general: it is some
conception of how to live in the way (or set of ways) that is good for
practical, rational primates like us. This substantive good or set of
goods is general enough to accommodate a variety of controversial
details about what one ought to do or not do. In other words, the
substantive view of practical reasoning allows for the possibility that,
in a disagreement, both parties are basically rational, while one party
may be more accurately identifying what is to be pursued or avoided.

Foot offers two additional considerations that support this Aristotelian
account. When she wrote her famous “Morality as a System of Hypothetical
Imperatives,” she argued that moral reasons are not overriding,
categorical imperatives contrasted with every other kind of reason. She
explains that, at the time, she had not discovered a way of showing “the
rationality of acting, even against desire and self-interest, on the
demand of morality.”[@foot2001natural 63] What changed her mind was an
argument from Warren Quinn to the effect that if practical reasoning is
to be important at all it must be *by definition* the pursuit of some
good. Quinn says:

> Practical thought, like any other thought, requires a subject matter.
> And for human beings the subject matter that distinguishes thought as
> practical is, in the first instance, human ends and action insofar as
> they are good or bad in themselves… Practical thought deploys a master
> set of non-instrumental evaluative notions: that of a good or bad
> human act, a good or bad human life, a good or bad human agent, and a
> good or bad human action. Practical reason is, on this view, the
> faculty that applies these fundamental evaluative
> concepts.[@quinn1993morality 223]

What Foot found so compelling is the change to “seeing goodness as
setting a necessary condition of practical rationality and therefore as
at least a part-determinant of [practical rationality] itself.” To one
who objects, she points out that:

> Many of us are willing to reject a ‘present desire’ theory of reasons
> for action because we think that someone who knowingly puts his future
> health at risk for a trivial pleasure is behaving foolishly, and
> therefore not well. Seeing his will as defective, we therefore say
> that he is doing what he has reason not to do. Being unable to fit the
> supposed ‘reason’ into some preconceived present-desire-based theory
> of reasons for action, we do not query whether it really is a foolish
> way to behave, but rather hang on to the evaluation and shape our
> theory of reasons accordingly. And it is exactly a generalization of
> this presumption about the direction of the argument on which I am now
> insisting. For what, we may ask, is so special about prudence that it
> alone among the virtues should be reasonably thought to relate to
> practical rationality in such a way?[@foot2001natural 63]

Quinn, Foot, and Frey are arguing that goodness is a “necessary
condition of practical rationality.” Rational action is action in
pursuit of some end, where “some end” is not merely an end (such as
food, friendship, or knowledge) that is intrinsically desirable for
practical rational primates like us. Identifying and pursuing such ends
*as desirable or undesirable* is already a substantive evaluative
judgment. Therefore, any rational action necessarily includes a
substantive evaluative judgment.

If we accept this point, and I do not see how to avoid it, then we are
already committed to a minimally substantive view of practical reason,
rather than a merely procedural one. The alternative to aiming at the
apparent good is not aiming at some value-neutral “end” or goal; the
alternative to aiming at the apparent good is *not acting at all*.

### On Motivation

While I summarized McDowell’s reply to the Humean critic above, I would
like to return to the subject of motivation here. It will be useful to
briefly situate my neo-Aristotelian account within the debate between
motivational internalists and externalists, even if I cannot adequately
engage the vast body of literature here.

In brief, the motivational internalist argues that any practical reasons
“out there” must necessarily connect up with my motivational structure
if they are to move me to action.[@williams2007internal] The
motivational externalist, by contrast, argues it is possible for there
to be practical reasons “out there” such that I *ought* to be motivated
by them, even if I am currently not. Indeed, the existence of binding
practical reasons that I am ignoring or failing to act on is the prime
explanation of immorality.

The danger of internalism is that it seems to allow that the amoralist
who is *not motivated* to be moral is off the hook. By contrast, the
externalist argues that the immoralist has *reasons* to φ even if she
has no (current) *motivation* to φ.

On my view, motivational internalism gets this much right: one is
motivated to pursue something that falls under a category that, within
the existing motivational structure, one *already judges* to be
desirable. However, the internalist too narrowly defines a “motivational
structure.” If by “motivational structure” we mean my present set of
broad psychological inclinations, then it is possible that we may not
have the right motivational structure that would lead to moral action.
But if by that we simply mean *my overall practical disposition toward
the worthwhile, desirable, and good*, then it is quite uncontroversial
to assert that one only goes in for φ-ing when φ-ing seems to be
worthwhile, because to be a practical agent just means to be oriented to
pursue the good and avoid the bad. Whatever may appear to me to fall
under the description of ‘good’ I will, ipso facto, be oriented toward
(whether I pursue it or merely approve of it and admire it). Whatever
may appear to me to fall under the description ‘bad’ I will, ipso facto,
oriented away from (whether I disapprove of it, or avoid it, or both).

What motivational externalism gets right is that there might be reasons
to φ that I am not aware of and (hence) am not motivated by. For
example, perhaps it is true that one ought to save for retirement, but I
may fail to do so because I am unaware of that reason or am ignoring it
in my attention to other reasons.

Seen in this light, it is obvious that on my neo-Aristotelian account
practical reasons can and do motivate us. We can put the matter more
strongly: according to Frey’s argument above, practical reasons are the
*primary* meaning of the term ‘motive.’ Motivation is (I argue) a
fundamentally rational state. It is true that sub-rational animals,
plants, and insects are moved about by impulses such as hungers,
thirsts, loves, fears, etc. And it is true that human animals are
likewise moved about by such impulses. But for rational animals, there
is an additional source of motion, namely practical reasons.

Hence, my contention is that our default view of practical reasoning
creatures ought to be that practical reason is intrinsically capable of
motivating. The whole process of discerning whether or not to φ is
theoretical in much the same way that the process of discerning whether
to believe that p, but it is also (by definition) practical. Practical
reasoning is not something one does *before* resolving what to do, as
one picks up an item in a store *before* purchasing it. Practical
reasoning is the name we give to the process of *resolving what to do*,
as checking out from the store is the process of purchasing. Just as the
appraisal of overwhelming evidence for p is not utterly distinct from
the affirmation that p, the deliberative conclusion that one ought to φ
is not utterly distinct from the decision to φ. To borrow Gibbard’s
unforgettable phrase, practical reasoning is “thinking how to
live.”[@gibbard2009thinking]

At the same time, there are goods we may not be pursuing (but ought to
be) and evils we may not be avoiding (but ought to be). We acquire new
motivations only when we successfully make new evaluative judgments
about what is to be pursued and avoided. Our fundamental motivation is
to pursue the good and avoid evil. We acquire *new* motivations when we
come to identify and affirm new practical reasons. These practical
reasons only motivate because they link up with the initial, existing
motivation.

### On Overriding Reasons

A final challenge that needs a response is this: moral reasons are
sometimes treated as “overriding” or “verdictive” reasons that settle
the question of what to do. Given the choice between, say, making a bit
of easy money by fraud or making the same amount through honest but hard
work, the prohibition against fraud is supposed to settle the matter. On
my account, do prudential practical reasons weigh just as heavily as
moral ones?

My answer is that the practical consideration that one ought never
commit fraud is, in such a case, certainly overriding. However,
sometimes prudential considerations are overriding, too. To take a
different example, suppose Smith comes into a bit of money from an
inheritance, and thus has a choice between spending it (innocently) on
world travels or allocating it to a solid retirement plan. Even if Smith
clearly needs more money in his retirement, the quandary ethicist would
have no *moral* recommendation, because neither choice is obviously
immoral in the sense that it violates one’s duties to others. The
character ethicist would: the practically wise person takes the
longer-term benefit of saving over the short-term benefit of traveling
to be overriding.

A normal human life presents practical reasoners with many situations in
which reasons pertaining to moral virtue (narrowly defined) play little
or no part. One must be sensitive not only to such reasons but to the
broad range of practical reasons. All practical reasons must be ranked
and weighed before a final, verdictive reason emerges. Any *reason to φ*
is a practical reason that can feature in an overall account of *what to
do*. What Anscombe calls “the verdictive ought” is simply what Foot
calls the thing to do “all things considered.”[@foot2001natural 57] It
often happens that one’s individual practical reasons conflict. McDowell
is incorrect to persist in labeling the broader process of adjudicating
such conflicts “virtue.” He ought to call it practical wisdom. The
practically wise person is the one who coordinates all other virtues and
executes them to good ends.

I should respond here to one final objection a reader might have. Has my
neo-Aristotelian view of practical reason defined away the possibility
of immorality? If everyone who acts is “aiming at the good,” doesn’t
this exculpate an agent’s apparently immoral motives or ends? For
example, someone might say, ‘It’s ridiculous to think that I always
pursue the good because I sometimes do wrong.’ This objection misses the
point. Of course practical reasoners sometimes do the wrong thing. The
proper response is that we perceive the bad *as overall worthwhile.* If
the immoral person acts wrongly, then he has misjudged the good. On the
neo-Aristotelian view, immoral acts are rational mistakes.

But it remains true that if the immoral person *acts at all* then,
according to the argument, he must by definition be pursuing some
apparent good. To be practically rational necessarily means to pursue
something *as good*, as desirable. Just as an epistemic agent might hold
a false belief p without affirming the false *as false*, a practical
agent might pursue a bad thing without pursuing it *as bad*. Rather, the
immoral person fails in their practical reasoning to correctly rank and
order specific goods. The imprudent person, for example, judges that it
would be better to eat, drink, and be merry today rather than plan to
avoid future ills. The cruel person judges that it would be better to
cause suffering than to be kind.

Someone might say, “But sometimes I perceive the bad *as bad* and pursue
it anyway.” My view is that we are sometimes able to include an end we
know to be bad into an overall set of practical reasons, which we still
judge is the thing to do, all things considered. One might judge, for
example, that smoking cigarettes is bad and still start if one judges
(with some conflict) that the potential pleasures overrule. (Having
become addicted to nicotine, the smoker’s judgment that the potential
pleasures *are not worth it* may not necessarily mean the smoker quits.)

I do not wish to suggest that identifying the thing to do is a smooth
and easy project. It is no more or less difficult than the project of
identifying what to believe is true.

The defendant of the procedural view is liable to point out that
reasoning about ends is even messier than such theoretical reasoning.
Indeed it is. But we must do it. People regularly argue, debate, and
reason about ultimate ends. Suppose Smith says to Jones, “I’m concerned
about you. You haven’t returned my calls. You lost your job, and you are
not eating. What’s wrong?” It would be no consolation for Jones to
respond, “Nothing’s *wrong*. I’m destitute, alone, and unhealthy, but
that is what I am *aiming* for.” Smith would rightly judge that
something had gone wrong for Jones to adopt such unhealthy and
ridiculous aims.

Practical wisdom is the paramount virtue of practical rational animals.
The upshot is that the foolish person – the habitually, incorrigibly
foolish person responsible for his own folly –  is, ipso facto, a bad
practical rational primate. He is failing to do *the thing to do*.

What is good in this sense for human beings is specific to our species.
The primary good of a kind for us is the human life form. The derivative
goods for us are any and all things necessarily related to the human
life form. In virtue of what we are, it is good for us to achieve
humanity, to become fully human. We aim to become what we are. That is,
we aim to become in actuality what we already are in potentiality. Some
of these goods are basic human goods toward which we are naturally
inclined: food, shelter, companionship, knowledge, etc. They are
starting points without which human beings would not be motivated to do
anything at all. \newline
\indent I should clarify that a thing’s status as a basic good is
revisable. The normal process of practical reasoning about what to do
can and sometimes does overrule the basic inclination toward a basic
good in pursuit of some alternative good. The point is that this
overruling judgment is not something over-and-above the practical
pursuit toward the good but another expression of the same pursuit. For
example, some people overrule their inclination toward the basic good of
human companionship by becoming solitary monastics but they only do so
in pursuit of *other* goods judged to be *better*. \newline
\indent Since practical reasoning is the process whereby we determine
the “sort of life that pertains” to creatures like us, all particular
practical reasonings about what to do in a given situation come to light
as parts of this whole. This fits with the account of virtue defended
above. There we saw that excellence in practical reasoning and rational
practice aims at doing well with one’s whole life. In other words, every
short-term choice fits into a context of long-term projects such as what
career to pursue, whether or not to marry, what friendships to maintain,
and so on. Furthermore, every long-term project fits into a broader
context of one’s answer to the maximally general question “how should
one live?”

Conclusion
----------

This chapter has defended in detail a neo-Aristotelian conception of
practical reasoning. It is an intrinsically normative and evaluative
process that defines the life form of practical, rational primates. On
my account, the structure of practical reasoning is akin to theoretical
reasoning. Whereas theoretical reasoning is by definition a normative
process in which the true is to be believed and the false to be
disbelieved, practical reasoning is by definition a normative process in
which good is to be pursued while evil is to be avoided. These “first
principles” are known by all functioning human adults. And while
particular rational inquiries aim at identifying good reasons to believe
or disbelieve a claim, particular practical inquires are aimed at
identifying basic goods intrinsic to human life. I argued that the
procedural view of practical reasoning is itself committed to certain
substantive normative judgments, including the judgment that *one ought
to do whatever will bring about one’s chosen ends*. More to the point, I
argued that the substantive view of practical reasoning is more
plausible: we reason about apparent goods and bads and act accordingly.
Nevertheless, my account leaves room for the commonsense insight that
success in practical reasoning (like theoretical reasoning) is by no
means guaranteed.

Success in identifying how to live and what to do requires a complex
process of adjudicating between all the available goods known to one,
sorting them, ranking them with care and wisdom, and forming them into a
complete life plan. The virtuous person knows what to do. Hence, contra
McDowell, practical wisdom is a kind of *practical knowledge* (a
“disposition to act well”) while other virtues (as discussed in chapter
4) can include rational practices and habits formed over time that
conduce to the realization of one’s life form. When practical reasoning
is well-functioning, it constitutes part of the natural excellence of
creatures like us. The vicious person is hindered by practical error —
or perhaps ignorance — of what to do. Success or failure along these
lines has a major influence on one’s other character traits. So
practical wisdom is an essential part of living a fully human life.

How should one live? A virtuous person’s answer to this question is not
just a proposition but a plan. More so, the virtuous person does not
simply *have a good plan* but *enacts* a good life plan. The answer is
not just a philosophy but a life.

Natural Reasoning
=================

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{Mountain peaks do not float unsupported; they do not even just rest upon the earth. They \begin{em}are\end{em} the earth in one of its manifest operations.}%
{---\textsc{John Dewey, \begin{em}Experience and Nature\end{em}, 3-4.}}
\centering
\end{epigraphs}
Is humanity just another instance of a biological organism, subject to
the same sort of evaluation as chimpanzees and dolphins, or is it a
different type of organism on account of exemplifying sui generis powers
of rational practice and practical reasoning? This question asks the
reader to give an account not only of the relation between humans and
other animals but an account of the relation between *nature* and
*reason*. The precise relation between nature and reason is an almost
intractable philosophical problem. Every major tradition – from Platonic
rationalism, Humean empiricism, Hegelian objective idealism, to Jamesean
neutral monism – presents a sophisticated stance on this relation.

The neo-Aristotelian account I have been developed aims to demonstrate
how human natural norms are instances of a broader category of natural
norms. These human norms are, for us, practical reasons. Human norms are
objective in that they provide normative guidance on how to live,
regardless of one’s awareness of or endorsement of them. Such norms
become *for the practical reasoner* when she correctly identifies them
as norms *for her*. Unless tragedy, injury, defect, and illness
interrupt the process, a young human being naturally matures into the
sort of practical rational primate that has at least *one* practical
reason: to do good and avoid evil. And every practical reasoner
naturally strives to acquire new practical reasons by asking the “how to
live?” question, thus adding to a growing stock of practical reasons.

The human norms I explored in the previous chapter – what Frey called
“primitive goods” – are perceptible by any human being who has grown
into adulthood and undergone a normal social process of formation.
Namely, the obligation to acquire traditional virtues such as courage,
moderation, and practical wisdom. These virtues represent good answers
to the question of how to live; one ought to develop such virtues in
oneself. Insofar as people acquire virtues, they overcomes the common
temptations to vice and practical folly to benefit themselves and
others; insofar as they succumb to vice and fall into practical
irrationality, they fail to realize their own life form and suffer the
intrinsic detriments thereof.

The account thus far developed has striven to be both *ethical* and
*naturalistic*. Recalling the dispute between Foot and McDowell, I have
argued that her sort of ‘organic naturalism’ is genuinely naturalistic.
The (apparently unique) ethical and rational norms intrinsic to living a
human life are of a piece with the kinds of norms intrinsic to a wolf or
white oak. Hans Fink points out that an ethical naturalist is “someone
who insists on a fundamental continuity between the ethical and the
natural.”[@fink 203.] Just how that continuity is to be cashed out is
the focal point of the dispute between Foot’s organic naturalism and
McDowell’s social naturalism.

One of the attractions of the Footian sort of neo-Aristotelian ethical
naturalism is that it provides a unified account of nature and human
nature. Foot’s concept of natural normativity – intrinsic to life forms
and natural ends – is a satisfying way of showing that continuity. For
Foot, normativity is not exclusive to practically reasoning creatures
like us. Every organism pursues its own goods – survival, reproduction,
and the exemplification of its proper life form. Julia Annas says:

> What is so helpful for ethics from this kind of biological naturalism
> is that we find that the normativity of our ethical discourse is not
> something which emerges mysteriously with humans and can only be
> projected back, in an anthropomorphic way, onto trees and their roots.
> Rather, we find normativity in the realm of living things, plants and
> animals, already. It is part of the great merit of the work of
> Philippa Foot… to have stressed this point. Like many important
> philosophical points, it is obvious once pointed
> out…[@annas2005naturalism 13]

Nevertheless, Foot’s organic naturalism is far from “obvious” to some.
One of the alleged drawbacks, according to John McDowell, John
Hacker-Wright, and others, is that “Foot’s naturalism draws on a picture
of the biological world at odds with the view embraced by most
scientists and philosophers.”[@hacker2009natural 308] McDowell endorses
bald naturalism when it comes to the “realm of law” that the natural
sciences study. Are natural norms – including human norms of practical
reasoning – simply outmoded by modern science? Though I have tried to
diffuse this worry in chapter 2, it is quite likely that something like
this concern remains. For the self-reflective nature of human life
creates special philosophical problems for the sort of naturalism I have
developed. Humans are aware of – and partially in control of – their own
life form and natural ends. Other organisms are not. Furthermore, when
we scientifically reason about other organisms, it is commonly thought,
we mostly describe. When we practically reason about ourselves, we also
evaluate. So how could practical reasoning be fundamentally the same as
descriptive, natural reasoning? The purpose of this chapter is to put
questions like this in a broader philosophical context and offer a
fuller response.\newline
\indent Section 1 sets up the discussion by presenting Chris Toner’s
four requirements that a successful neo-Aristotelian naturalism must
meet if it is to overcome the sort of criticisms McDowell poses. I
provide further details on how my account thus far has already satisfied
three of the four.\newline
\indent Section 2 argues that McDowell’s alternative to Footian
naturalism fails to satisfy Toner’s fourth requirement. I detail
McDowell’s concepts of first and second natures. Since his paradoxical
views have caused some consternation among his philosophical readers, I
first offer an explanation of his beguiling metaphilosophical project. I
then explain how he deploys these concepts in his ethical project.
\newline
\indent Section 3 brings multiple charges of inconsistency against
McDowell’s account of nature. First, he seems to both deny and affirm
that some relational properties (such as *meriting*) are part of primary
nature. Secondly, drawing from Hans Fink to distinguish different
concepts of nature and scientific reasoning, I argue that McDowell’s
conception affirms two conflicting concepts. On either of two plausible
conceptions of nature and the natural, my account demonstrates that
practical reasoning is natural reasoning. Thirdly, McDowell’s account
unwittingly falls into the very sort of undesirable nature/human dualism
he emphatically wishes to avoid. Fourthly, McDowell’s intersubjective
notions of both scientific and ethical reasoning lead to an incorrigible
relativism. For each inconsistency, I show how my accounts of virtue and
practical reason (developed in chapters 4 and 5) are more adequate to
the task of meeting Toner’s fourth requirement. I suggest “recursive
naturalism” as an appropriate name for my view, since human beings are
natural organisms able to practically reason about nature, about
themselves, and about practical reasoning itself.

Four Requirements
-----------------

A recent article by Chris Toner argues that neo-Aristotelians (such as
Foot and Michael Thompson) have not yet adequately responded to
McDowell’s objections and satisfied four requirements “naturalism must
deliver if it is to support a revived Aristotelian virtue
ethics…”[@toner2008sorts 222] Fortunately, our account thus far has
satisfied three of the four.

The first requirement is that *natural norms must be intrinsically able
to motivate the bearer of the nature.* Put differently, the natural
human norms pertaining to our nature must be, for us, practical reasons.
In chapter 5, I argued that practical reasons, by definition, motivate
us. Practical reasoning is not simply one of many ways we can be
motivated; it is the very capacity to be motivated by reasons. Practical
reasoning is, of course, not the only way we can be *moved*. Plants and
animals are inclined or moved to their good by unreasoning genetic
“programs,” instinct, fear, irrational appetite and so on. They are
moved but have no further capacity to take these sources of movement
*as* practical reasons. Humans are inclined toward their good *both* by
the same impulses (instinct, emotion, desire, etc.) *and* by practical
reason. I also argued that the first object of human practical reasoning
is a quite general conception of what is to be done and pursued (the
good) and what is to be avoided (evil). By ‘good’ we did not mean a
non-natural entity or property apprehended theoretically but any natural
entity or property apprehended *as* choice-worthy, desirable, or
to-be-pursued. As Frey clarifies:

> Although natural inclinations depend upon conceptual apprehension, we
> should not be tempted to think that they are objects of contemplation.
> These goods, as first principles of practical reason, are apprehended
> as ends – as objects of pursuit rather than as objects of
> contemplative knowledge.[@frey 88]

The objects of pursuit are many: friendship, knowledge, money, pleasure,
and so on. I did not attempt to give a complete objective list. I rather
argued that the natural human norms pertaining to our life form are on
on the list. While there are many actions of humans, there is only one
kind of human action: the unique process of taking natural inclinations
and natural norms as prima facie practical reasons, reflecting on them,
and organizing them all into a rational plan for what to do, all things
considered.

This conclusion goes a long way to solving what Jennifer Frey calls the
“Irrelevance Problem.” She says:

> [Irrelevance] is a more sophisticated presentation of the so-called
> ‘naturalistic fallacy.’ But rather than crudely rejecting any move
> from ‘is’ to ‘ought’, it merely blocks the inference at one crucial
> juncture—the inference from the ‘is’ of the species, to the ‘ought’
> that governs the rational will.[@frey 14]

As we saw in chapter 5, McDowell argues that – granting the existence of
natural human norms to seek food, shelter, comfort, survival, society,
and so on – these norms are not necessarily binding. His discussion of
the “rational wolf” illustrates the objection.[@mcdowell1998two]
Although a wolf is “supposed to” hunt in packs because that is a formal
property of its nature, if a wolf were endowed with *logos* it would be
just as free as human beings are to step back from such natural norms
and either endorse or reject them. Nevertheless, even this higher order
adjudication is subject to natural norms of practical reasoning. A
practical rational primate ought to order her natural inclinations
according to what is, all things considered, good for human beings. Even
though I find within myself the desire, say, to eat good food, such
norms direct me to eat certain things at certain times and in certain
ways. A habitual glutton might feel a craving to overeat between meals,
but decide that, all things considered, it is better to be moderate. Or
an anorexic might feel psychological pressures to eat too little, but
decide that, all things considered, it is better to eat a sufficient
amount.

Toner’s second requirement is this: *natural norms must be intrinsically
able to justify themselves to the bearer of the nature.* Natural human
norms must not be merely given; they must somehow justify themselves.
Reflection must reveal that the norms are *good* practical reasons to
all rational agents. The norms need not, Toner admits, *automatically*
persuade a Callicles to repent of his wickedness. However, they must be
*able to* become justifiable motivations under normal circumstances. He
says:

> …I say “intrinsically able to motivate or justify” rather than
> “intrinsically motivating or justifying”: the natural norm is such
> that it can motivate or convince persons, provided they are not in too
> dysfunctional a state. In the same way a rose is such as to be
> intrinsically able to convince us of its being red. Its failure
> actually to do so in my case because I am color-blind or jaundiced
> does not impugn this intrinsic ability. Natural norms can motivate and
> convince because they are neither “mere facts” about the way a given
> species does go on nor “brute desires” a given species happens to have
> as a result of its evolutionary history.[@toner2008sorts 235]

It is true that mere general descriptive facts do not motivate and that
simple brute desires to behave in a certain way are not necessarily
overriding motivators. However, as I have argued in chapters 2 and 3,
natural norms are not reducible to either mere facts or brute desires.
Rather, natural norms both characterize what traits count as virtues for
practical rational creatures like us *and* they are intrinsically able
to justify themselves to the bearers of that nature.

This requirement affords the opportunity to respond to what Elijah
Millgram calls the “Pollyanna problem,” according to which any honest,
empirical assessment of human natural norms would include vicious norms
as well as virtuous ones because justice and injustice are both
statistically “normal.”[^63] Anscombe anticipates this worry when she
says:

> The search for “norms” might lead someone to look for laws of nature,
> as if the universe were a legislator; but in the present day this is
> not likely to lead to good results: it might lead one to eat the
> weaker according to the laws of nature, but would hardly lead anyone
> nowadays to notions of justice.[@anscombe1958 14]

Millgram et al., might object that I was winking at the dark side of
human nature when I built my inductive case for the generic that the
human beings are practical rational primates. After all, empirical
sociology can establish the truth of such generics as: politicians lie,
sociopaths murder, businesses cheat, criminals steal, countries wage
unjust war, parents abuse their children, and so on. Likewise, empirical
biology shows that some acorns become fully grown, mature oaks, but
other acorns become stultified, sickly specimens. (Most acorns never
become anything other than acorns before they disintegrate into dust in
the soil.) Some animals protect their young while other animals abandon
or even consume their young. Are we supposed to allow, then, that “Human
beings abandon their young” is a generic truth, indicative of the human
life form? Are we obligated to fulfill all such norms? Just some? Which
ones?

I think this problem, while important, is ultimately specious. In order
to even pose the objection, Millgram et al. have to discriminate between
good and bad norms. Millgram cites such traits such as dishonesty,
infidelity, and cruelty that are statistically prevalent but obviously
immoral. The neo-Aristotelian can agree with his evaluation.
Furthermore, good norms are not mere statistical generalizations. When
we examine the behaviors of organisms, we begin with making
generalizations. Even constructing scientific accounts of organisms, we
do not stop there, but sift through them. Some remain mere
generalizations about how some creatures happen to behave, while others
are classified as essential or natural to how that creature behaves. The
latter are natural norms. I have already argued that a good example of
such natural norms is that humans are practical rational primates who
mature into practically wise and virtuous agents. But I do not mean that
every such example is easy. How should criminals be punished? What kinds
of sexual practices are acceptable? How should societies relate to one
another? Aristotle points out that raiding neighboring tribes is a
near-universal form of wealth-acquisition and concludes that it is
natural – i.e., morally acceptable. I would object that only mutual
respect and arms-length trading (which are also statistically common)
are morally acceptable. Natural human norms are not necessarily easy to
identify. The point is that disputable cases are disputes over the very
question of which behaviors are essential and which unnatural.

Furthermore, we do not need to concede a fundamental discontinuity
between the kind of discrimination between good and bad norms essential
to ethical reasoning and the kind of discrimination between normal and
pathological that is essential to biological and other scientific
reasoning. Rather, the process of sifting between various
generalizations is one and the same, whether in scientific or ethical
accounts. Moral and rational defects can be overwhelmingly common.
Regardless of how statistically common the failure to conform to such
norms, the discernment between virtuous and vicious is akin to the
discernment between healthy specimens and unhealthy ones, normal animals
and pathological ones. Indeed, part of having a properly-formed mind is
that one can distinguish between natural norms and mere generalizations.

For example, the *National Geographic* narrates how a sloth bear in
Washington D.C. gave birth in captivity to three cubs. The first one was
immediately killed and eaten by the mother, but the second and third
cubs were nurtured and cared for. The zookeepers were appalled. When,
after a week of caring for the remaining cubs, the mother killed and ate
another, they intervened to save the third.[^64] This event posed the
question: is something wrong with the mother bear? First, the zookeepers
observed the facts: the mother ate one cub and nurtured (temporarily)
the other two. Then they made two quite different generalizations: (1)
mother bears care for their young, and (2) mother bears kill and eat
their young. The contradiction demands sifting. The zookeepers then
discerned which is the natural norm. University of Southern California
primatologist Craig Stanford points out that the consensus among
biologists is to affirm the generic truth: a mother cares for her young.
As a normative generic, we can say without a change in meaning that a
mother bear is *supposed* to care for her young, and hence that
infanticide is pathological. New data can confirm or disconfirm this
evaluative judgment. For instance, the third cub of the sloth bear whom
the zookeepers intervened to save turned out to suffer an elevated white
blood cell count. It is possible that the other cubs were sick as well.
The zookeepers speculated that the mother somehow knew this and so
killed the ailing cubs. If this were true, it would give rise to a new
normative generic: a mother cares for her healthy young. If it turned
out that the two other cubs were *not* in fact ailing, the mother’s
behavior would be classified as pathological.

Similarly for humans and other primates.[@goodall1977infant]
Psychologist Christine Lawson narrates the horrifying story of when a
mother drowned her two young children in order to ingratiate herself to
a man she was dating who said, offhandedly, that he did not want
children:

> [In 1992,] Susan Smith drove to a lake near Union, South Carolina, and
> parked her car at the top of a boat ramp. She stepped out of the car,
> released the parking break, and let the car roll into the water with
> her babies strapped inside. Covering her ears with her hands so she
> could not hear their screams, she ran up the ramp as the car rolled
> toward the lake. It took six minutes for the car to sink, drifting
> away from the ramp, bobbing nose first into the
> water.[@lawson2000understanding 122]

The father of the children, Susan’s ex-husband, shared his recollection:

> There were some troubling things that I learned in the aftermath of
> the killings… There’s only one conclusion I could make. Susan watched
> the car as it sank. This was too awful, too terrible to imagine. Susan
> waiting, seeing Michael and Alex die. If that were true, there is no
> doubt something truly evil in Susan’s character, something
> unspeakable.[@lawson2000understanding 122]

Statistically, the vast majority of human parents do an adequate job,
but we do not posit “parents care for their children” as a mere
statistical likelihood that admits of exceptions. Rather, psychologists
correctly judge such exceptional cases of parental indifference and
cruelty as normative errors. This particular parent was not merely a
statistical anomaly but an example of a psychological disorder (in this
case, Borderline Personality Disorder). Understanding and labeling her
disorder should not lead us to soften the normative evaluation of her
actions. (Many Borderline parents manage their disorder and do an
adequate job in spite of it.) Susan Smith’s behavior was criminal, but
it was also pathological and – as David Smith said, truly evil. Lawson
explains that “Susan Smith sacrificed her children in order not to be
abandoned by her boyfriend, the wealthy heir to the town’s largest
industry.”[@lawson2000understanding 123] To take a significant other’s
offhand comment about not wanting children *as a reason* to murder one’s
own is a devastating error in practical reasoning. The correct practical
reasoning is almost too obvious to need stating: There is *good reason*
to take care of one’s child. Parents are *supposed to* care for their
young, even when doing so is difficult or costly. These natural norms
seem to me excellent examples of the sort of natural norms that are
intrinsically able to justify themselves to the bearer of human nature.

The same pattern holds when constructing norms pertaining to a whole
host of virtues. As Toner mentions, “The requirements of the virtues can
be articulated into what Hursthouse calls v-rules (do what is just, what
is courageous, and so forth).”[@toner2008sorts 242] I would articulate
such norms or “v-rules” in the form of generics: human beings do what is
just, what is wise, etc. The generic picks out what human beings
naturally do; the failure to it is, accordingly, a defect.

Toner’s third requirement is this: *natural norms must be anchored in
and express universal human nature.* In chapter 3 I defended a
definition of “universal human nature,” that we are practical rational
primates. And I argued that the natural norm that one ought to become a
fully mature practical rational primate (as represented by virtuous and
wise exemplars) is successfully “anchored in” that nature. More
specifically, all the virtues of rational practice and practical
reasoning are examples of such norms. For, as Toner says:

> … the possession and exercise of the virtues is essential to human
> flourishing as dependent rational animals. Thus natural norms or the
> requirements of the virtues, in articulating what we need (to have, to
> be, to do) to flourish, are anchored in and express universal human
> nature.[@toner2008sorts 242]

There are many examples of natural norms that philosophers plausibly
take to be intrinsically justifying to human beings. I mentioned in
chapter 4 a few examples from Russ Shafer-Landau, such as that “it is
wrong to take pleasure in another’s pain, to taunt and threaten the
vulnerable, to prosecute and punish those known to be innocent, and to
sell another’s secrets solely for personal
gain.”[@shafer2003moralrealism, chapter 11] Richard Boyd follows Hilary
Putnam in calling such norms “quasi-analytic”:

> Indeed, many fundamental scientific laws (as well as some scientific
> truisms) and many fundamental moral principles have the property which
> we might call quasi-analyticity (see, e.g., Putnam 1962). Because of
> their conceptual and methodological centrality, even when we know that
> their justification is a posteriori rather than a priori, we find it
> extremely difficult to envision circumstances under which they would
> be disconfirmed. For as long as they occupy so central a conceptual
> and methodological role, they are immune from empirical revision, and
> principles incompatible with them are ineligible for empirical
> confirmation (let’s call them quasi-analytically ineligible). As
> Putnam indicates, quasi-analyticity and quasi-analytic ineligibility
> can be altered only by pretty serious conceptual and theoretical
> “revolutions,” whose directions are all but impossible to anticipate
> prior to the innovations or crises which precipitate them. The
> principle that torturing children is wicked and the fundamental laws
> of quantum mechanics are both candidates for
> quasi-analyticity.[@boyd2003finite 520]

I think Boyd and Putnam are correct here. Some ethical laws are on a par
with some scientific laws in being pretty well incorrigible. While the
west has undergone “conceptual revolutions” that have overturned
deeply-held traditions such as, say, slavery or the torture of
prisoners, we can point to even deeper quasi-analytic principles that
have never undergone revolution in the west or (to my knowledge)
anywhere in the world: the importance of caring for children, the value
of truth. One can find persons and societies that *in fact* violate
these norms, but not that *in principle* believe children should be
corrupted and that everyone should deceive themselves and others.

If quasi-analytic ethical laws indeed exist, the question is how to
explain this. Recalling Frey’s discussion of Aquinas “first principle of
practical reason” can help us to draw the proper relation between these
norms of morality and norms of practical reason. That fundamental
normative principle was that good is to be done and pursued, and evil is
to be avoided. This principle provides the major premise for a practical
syllogism behind every rational action, where the minor premise is some
virtually unrevisable evaluative judgment: e.g., evil is to be avoided,
and torturing children is evil, therefore torturing children is to be
avoided; good is to be pursued, loyalty is good, therefore loyalty is to
be pursued. Practical irrationality does not arise when one judges that
good is to be avoided and evil pursued but when one makes a fundamental
mistake about what is good or evil and, hence, judges it to be the thing
to do.

Toner’s fourth requirement is this: *first and second nature must be
related so that the second is a natural outgrowth of the first, and so
that that in our given makeup is (first) natural which does tend toward
an ethically mature second nature.* While McDowell believes that his own
alternative to Footian naturalism more adequately meets this
requirement, I believe that a consistent reading can show that his
account falls short.

First and Second Nature
-----------------------

Recall the quotation from chapter 1 that explains McDowell’s objection
to Foot’s organic naturalism. He says:

> I doubt whether we can understand a positive naturalism in the right
> way without first rectifying a constriction that the concept of nature
> is liable to undergo in our thinking. Without such preliminaries, what
> we make of ethical naturalism will not be the radical and satisfying
> alternative to Mrs Foot’s targets that naturalism can be. Mrs Foot’s
> writings do not pay much attention to the concept of nature in its own
> right, and this leaves a risk that her naturalism may seem to belong
> to this less satisfying variety.[@mcdowell1998mindvalue 167]

McDowell makes clear that his dispute with Foot concerns her “concept of
nature.” McDowell’s picture of the relation between nature and reason
appeals to “second nature.” He says he aims to “formulate a conception
of reason that is, in one sense, naturalistic: a formed state of
practical reason is one’s second nature, not something that dictates to
one’s nature from outside.”[@mcdowell1998two] McDowell is an ethical
naturalist in that he also insists on a “fundamental continuity” between
the ethical and the natural. It is clear that he does not wish to fall
into a dualism between biology and rationality. Nevertheless, it seems
to me, he sets up another equally pernicious dualism.

In order to make good on this criticism, it would be prudent to first
put McDowell’s ethical project in metaphilosophical context. McDowell is
a proponent of “therapeutic philosophy.” He says he is influenced by two
main sources: the “Socratic tradition” and
Wittgenstein.[@mcdowell1998mindvalue, preface] From the Socratic
tradition he draws a way of thinking in which dualisms do not even
arise. And from the later Wittgenstein he draws a way of doing
“therapeutic” philosophy – philosophy that ‘leaves everything as it
is.’[^65] McDowell believes many philosophical puzzles arise not from
the puzzling nature of reality itself but from errors in *our own
thinking*, so we need “therapy”: dualisms need to be *exorcised*. He is
both an anti-realist and an *anti*-anti-realist. He is therefore always
fighting on two fronts, attacking a position while trying to avoid
supporting its apparent opposite.

This feature of his thought is liable to puzzle and even frustrate some
philosophers.[For examples of both puzzlement and genuine frustration,
see @mcdowell2008critics] A bit of context can help make his project
comprehensible in both its ethical and metaphysical expressions. For
example, consider his philosophy of mind. In *Mind and World* he
attempts to dissolve the “vacillation” between naive empirical realism
(compare with: Footian organic naturalism) and “Rampant Platonism”
(compare with: non-naturalism) by arguing that even primary qualities
are not given to us in experience without the involvement of spontaneous
conceptual capacities. He wants to accept the modern scientific picture
of nature as “bald nature,” a mechanical “realm of law,” disenchanted
from values, norms, ends, and reasons. But he does not want to accept
that human rationality is likewise mechanical. Instead, he argues that
humanity exists in a space of reasons where we recognize reasons for
belief and reasons for action.

Even in *Mind and World*, his solution depends on a neo-Aristotelian
conception of human beings as practical reasoners. Understanding human
reasoning in contrast to nature “requires a different conception of
actualizations of our nature.”[@mcdowell1996mind 77] In that book, he
deploys the concept of “second nature” to describe the way human beings
are initiated into particular ways of behaving and knowing by *Bildung*
– that is, by education, formation, or cultivation.[^66] Practical
wisdom is one example of a virtue that the young human being does not
have but that may be developed by formation. At first, the ethical
demands of practical wisdom are not even perceptible to the young. They
have the natural potential to become aware of (and answerable to) the
demands of practical wisdom. Slowly, that potential is actualized or
inculcated and a moral outlook is attained. Human beings are initiated
into this stretch of the space of reasons by ethical upbringing
(Bildung) which instills the appropriate shape in their lives. So
initiated, practically wise behavior is not just a new kind of behavior
but the maturation and development of a new kind of faculty in the human
animal. He says that “[The ethical demands of reason] are essentially
within reach of human beings. So practical wisdom is second nature to
its possessors.”[@mcdowell1996mind 84] In this sense, a mature human
being can be rightly described as “doing what comes naturally” when she
engages in certain rational activities that have been deeply habituated.

McDowell’s ethical writings employ the same solution expressed in almost
the same terms. For example, “Values as Secondary Qualities” argues
against both anti-realism and anti-anti-realism, but instead of opposing
a vacillation between empirical realism and rampant Platonism, he
opposes a vacillation between Footian naturalism and pure subjectivism.
Instead of arguing that even primary qualities involve spontaneous
conceptual capacities, McDowell argues that even the identification of
values involves the subjective or intersubjective capacity to create
value.

Subjectivists such as Mackie, Allan Gibbard, and Simon Blackburn believe
that normativity is “projected” by philosophers and scientists onto the
natural facts. McDowell grants that Mackie et al. are right to assert
that values, like secondary qualities, cannot be adequately conceived
“except in terms of certain subjective
states.”[@mcdowell1998valuessecondary 139] There is no such thing as
“to-be-pursuedness” existing as a Lockean primary quality in first
nature. Whereas Foot thinks that normative facts are
response-independent features of (first) nature, McDowell dismisses this
possibility out of hand. He says that naive realism about value is
“impossible – at least on reflection – to take
seriously…”[@mcdowell1998valuessecondary 132] In considering the notion
of intrinsically normative natural facts impossible to take seriously,
McDowell agrees with Mackie: the “central doctrine of European moral
philosophy” is a mistake;[@mackie] it is wrong to think that some things
*merit* certain responses by virtue of what they are and what we are.

A reader unfamiliar with McDowell’s metaphilosophical project might
conclude that he must think values are not objective features of nature
and hence that they are purely subjective. But it does not necessarily
follow that values are illusory projections onto the world. A secondary
quality is not “a mere figment of the subjective state that purports to
be an experience of it.”[@mcdowell1998valuessecondary 136] The problem
with subjectivism is that it misses the way in which “ordinary
evaluative thought [is] a matter of sensitivity to aspects of the
world.”[@mcdowell1998valuessecondary 131]

McDowell’s alternative presents first nature as consisting of both
Lockean primary qualities, which are response-independent, and Lockean
secondary qualities, which are response-dependent dispositional
properties. Colors and values are natural in the sense that they are
dispositional properties. Color-properties must be defined partly by
their “objective” or response-independent aspects and partly
phenomenologically. It makes no sense to speak of what *redness is*
apart from perceptions of red *in perceivers*. Similarly, he argues, it
makes no sense to speak of “dangerousness” apart from a subject who is
potentially vulnerable or “rightness” apart from a subject who
potentially judges the value of a thing. Even so the property of “being
such as to look red” may or may not *have ever been perceived as red* by
any observer (if, for example, the appropriate conditions have never
obtained). So a Lockean secondary quality may be response-independent in
some sense, but it is not *redness as such*. It is the dispositional
property that is disposed to present us with an appearance of a
particular phenomenal character. In the same way, goodness, badness, and
other values are grounded in “second nature.”[@mcdowell1998two 188 and
following.] The space of reasons in which our rational capacities
operate makes us sensible to those dispositional properties of primary
nature which become, for us, values such as goodness and badness. And,
as we saw in chapter 5, he thinks that the normativity of theoretical
and practical reasoning is merely grounded in our shared form of life.

Inconsistencies
---------------

McDowell’s view is, I think, ingenious, but vulnerable to at least four
criticisms. First, McDowell thinks that treating practical reasons as
primary qualities of nature is “impossible to take seriously” because he
wonders “how something that is brutely *there* could nevertheless stand
in an internal relation to some exercise of human
sensibility.”[@mcdowell1998valuessecondary 132] Is this really so hard
to imagine? We can find an example of this mundane relation in his own
article.

To illustrate his point about human responsiveness to value, he presents
an analogue in the animal kingdom which he (somewhat playfully) labels
his “theory of danger.” His theory of danger is that there is something
about predators, say, that is really dangerous to their prey. The
immanent presence of a bear does not just cause fear in a rabbit but
*merits* it. To describe a bear as dangerous to rabbits is to assert
something about both bears, about rabbits, and about their place in the
animal kingdom on our planet. The rabbit does not need to use concepts
or make rational judgments to see the bear as dangerous; it merely needs
its natural perceptual capacities and its instincts. When a prey
observes a predator, it feels fear; but the fear-response is not
obviously reducible to a perception of some purely descriptive property,
such as the bear’s fur (other non-predators have fur) or its size (other
non-predators are just as large or larger). Nor is “dangerousness”
something projected by the rabbit onto the bear. Rather, the fear arises
in response to the danger, or perhaps the bear-as-dangerous. Likewise,
to describe a particular food as disgusting (say, rotten fruit) is to
assert something about humans, about rotten fruit, and about the
relation between the two. Given the kinds of beings we are, and given
the natural properties of rotten food, the fact that we ought not to eat
it seems to be a straightforward, natural normative fact. The brute
presence of a bear stands in an internal relation to the exercise of the
rabbit’s natural sensibility: it had better run. In humans, the brute
fact that parents have a child stands in an internal relation to the
exercise of our natural, rational sensibility: they had better care for
the child.

### Restricted or Unrestricted?

Secondly, McDowell thinks the Footian sort of naturalism (which he
called “naive realism”) is impossible to take seriously because he
thinks the view of that nature consist of both descriptive and some
normative primary qualities is inconsistent with modern science. He
says, “The most striking occurrence in the history of thought between
Aristotle and ourselves is the rise of modern science.”[@mcdowell1998two
174] Although he thinks Aristotle provides the right cues, the modern
scientific picture of nature is “disenchanted” from intrinsic moral
values or human norms.

In *Mind and World*, he expresses his view by saying that human beings
“partially re-enchant” nature. Perhaps this is why some have objected to
McDowell’s account of the relation between nature and reason as being
insufficiently naturalistic. For example, James Lenman says: “McDowell
is certainly pervasively inspired by Aristotle and he describes himself
as a naturalist. See especially his 1995. But I suspect many
philosophers would find his use of the term ‘naturalist’ here somewhat
Pickwickian.”[@sepmoralnaturalism, section 4.1, footnote 18.] The ‘many
philosophers’ Lenman alludes to are probably physicalists or
materialists. Physicalism is indeed a paradigmatic sort of naturalism,
and McDowell is a staunch critic of physicalism. Nevertheless, I shall
try to show that McDowell’s view also has rightful claim to that title.
McDowell’s flaw is not an idiosyncratic definition of ‘nature’ but an
inconsistent one.

Before we consider McDowell’s definition of ‘nature, we should ask: how
do philosophers commonly deploy the term? Russ Shafer-Landau does an
adequate job of exposing the flaws in a variety of common ways of
stipulating what ’natural’ means:

> Something is natural just in case, necessarily, it is . . . what? It
> isn’t such as to be touchable, or tangible. Being a species isn’t
> touchable. Neither is being a quark. Being natural is not the same as
> being non-conventional: moral properties, if non-naturalists are
> right, are certainly that. It isn’t the feature of being material:
> certain physical fields, or vacuums, are natural in anyone’s book, and
> yet not composed of matter. It isn’t the feature of being causally
> efficacious: being such that everything is either red or not, being
> divisible by itself, and being self-identical are causally inert
> natural properties. Being natural is not the same as being a feature
> of the world prior to, or considered apart from, the presence of
> humans. For being human, or a human artefact, is a natural feature.
> Nor can we define a natural property as any property that is not
> evaluative. For moral properties are evaluative on anyone’s reckoning,
> and so we would, by definitional fiat, thereby rule ethical naturalism
> out of court. It can’t be got rid of as easily as
> that.[@shafer2003moralrealism 58-59]

Some readers may object to the level of detail at which I attempt to
capture a definition of ‘nature.’ They might insist we must simply
stipulate our definition of ‘nature’ and move on. I rather think it is a
scandal that so many writers pass over such weighty matters with pithy
commonplaces rather than rigorous definitions. Although Shafer-Landau’s
discussion of nature and naturalism is exceptionally thorough, he is
still forced to settle on a “disciplinary” definition of the natural:

> Naturalism… claims that all real properties are those that would
> figure ineliminably in perfected versions of the natural and social
> sciences. Since we don’t have any of those versions in hand, we can’t
> be absolutely sure about our naturalistic
> inventory.[@shafer2003moralrealism 59]

The indeterminacy of such a disciplinary definition of the natural is
unsatisfactory for someone defending the ‘naturalism’ of a theory
against the accusation of ‘non-naturalism.’ When it comes to such
important and highly ambiguous concepts as nature and science, much more
is needed. Hans Fink is right to say that “this is a terminological
issue, but it is not easy to resolve simply by choosing one’s definition
of ‘nature’ and then sticking to it.”[@fink 206] Fink continues:

> No account of naturalism should forget the fact that ‘nature’ is, as
> Raymond Williams puts it, ‘perhaps the most complex word in the
> language’ (Williams 1981: 184), or as Hume puts it, a word ‘than which
> there is none more ambiguous and equivocal’ (THN: III.I.II.)…Indeed,
> it is a deep root of ambiguity that we can talk about the nature of
> art, law, language, culture, morality, normativity, history,
> civilization, spirit, mind, God, or nothingness even if we otherwise
> regard these as non-natural, that is, as not belonging to nature as a
> realm. There is no contradiction in talking about the nature of the
> unnatural, the super-natural, or the non-natural, just as it is an
> open question what the nature of the natural is.[@fink 206]

In short, the concept of nature is treacherously ambiguous. For the
remainder of this section, I shall summarize the key details of Hans
Fink’s essay on the topic, which clears up much of this ambiguity. Then
I shall show how McDowell embraces two mutually incompatible options.

Fink begins by pointing out that there are at least two broad kinds of
conceptions of nature: The first is “Unrestricted nature” a conception
which leaves nothing out. Fink explains the unrestricted conception in
this way:

> [The term ‘unrestricted nature’] would express the idea that there is
> one world only, and that that world is the realm of nature, which is
> taken to include the cultural, artificial, mental, abstract and
> whatever else there may prove to be. There are no realms above or
> beyond nature. To be is to be in nature and to be in continuity with
> everything else in nature. Even the greatest and deepest differences
> are differences within nature rather than differences between nature
> and something else.[@fink 206]

The alternative to unrestricted nature is (2) “restricted nature.”
Restricted nature picks out some subset of things as natural, exclusive
of anything ‘non-natural,’ unnatural, or supernatural. Unrestricted
naturalism is ecumenical. Restricted naturalism is parsimonious.
Unrestricted naturalism is simple. Restricted naturalisms are legion.
For example, Fink lists eight different conceptions by which one can use
‘natural’ to distinguish from the non-natural: the world unaffected by
intelligent intervention (e.g., the arrangement of trees in the Yukon)
is natural as opposed to the world so affected (a row of trees along a
city street). Or, as Fink says, ‘nature’ could refer to “the empirical
world as opposed to the intelligible world of the abstract, logical, or
mathematical.” And there are several other ways in which the restricted
conception can be cashed out.

The advantage of the unrestricted conception is that it does not try, in
advance, to stipulate what is and is not real. This can do the trick of
resolving disputes about what is natural. As Fink puts it, “Nothing less
than a naturalism that deserves to be presented as absolute could help
break the spell of bald naturalism without merely replacing one
restricted sort of naturalism with another and thus keeping the
oscillations going.”[@fink 219] On unrestricted naturalism, even
culture, art, rationality, intelligent intervention, and so on are parts
of reality. Fink’s comment on the John Dewey passage in the epigraph
above is this:

> On this conception the aesthetical (and the ethical) are not
> independent of nature, but they are not somehow based on nature or
> supervening on it either; rather, they simply are nature in some of
> its manifest operations. To think otherwise is both to mystify the
> aesthetical (and ethical) and to trivialize nature. The man-made, the
> artificial, the cultural, the historical, the ethical, the normative,
> the mental, the logical, the abstract, the mysterious, the
> extraordinary, are all examples of ways of being natural rather than
> examples of ways of being non-natural. Nature is never *mere* nature.
> That which is *more* than *mere* is nature, too.[@fink 217]

The disadvantage of the unrestricted conception is that it is
tautologous: one can no longer use the accusation of “non-naturalism” as
a weapon against opponents with a competing ontology. It obviously makes
no sense to criticize someone for positing entities “over and above”
nature after defining “natural” as “real” and hence “non-natural” as
“unreal” by definition. As Stephen Brown says, “If by ‘nature’ we mean
‘everything that is,’ then of course there is nothing outside
nature.”[@brown2008virtue 2]

The advantage and disadvantage of the restricted conception is the same:
on the one hand, we can classify some entities as non-natural in
advance, and exclude or bracket them; on the other hand, we are
obligated to provide a principled justification for the classification
of unfavored entities that doesn’t, at the same time, exclude some
favored entities. Fink’s discussion of Plato’s *Laws* shows how tricky
this classification can be. In the *Laws*, the Athenian distinguishes
three kinds of events and three corresponding kinds of causal
explanation. First, the growth of plants and the orbit of the sun etc.,
come about by nature (*physis*). Second, anything that does not come
about by nature or art comes about by chance, e.g., leaves fall into
this or that pattern and mountain ranges form into this or that shape,
etc.. Third, houses have roofs and humans wear clothes by art.

The Athenian then asks, which of these three types of events are
“natural”? The first hypothesis, which he eventually rejects, is that
the first two are natural – namely, nature and chance. They are natural
because they come about prior to and independent of intervention from
humans or gods. By this classification, however, the natural excludes
not only the supernatural but the cultural, the fictional, the
aesthetic, and so on. The Athenian calls this conception of nature
“dangerous” because it makes everything having to do with intelligence
non-natural.

The second hypothesis, which the Athenian defends, is that the third
kind of event (art) is the natural kind. He tries to prove that soul is
ontologically prior to body. He says that “soul is necessarily prior in
origin to things which belong to body, seeing that soul is older than
body.”[@plato, *Laws* 891cff] He first defines ‘soul’ as self-movement,
and the cause of motion in other things, and ‘body’ as the things moved.
Regardless of the merits of the Athenian’s argument, it should be plain
that the two hypotheses agree that the “natural” kind of event and cause
is the *primary* one. Even though the Athenian’s thesis is “pretty
rampant Platonism,” Fink points out that it is “clearly presented as an
account of the soul as natural because primary in existence… mind is
prior to world.”[@fink 215] To illustrate the point, he shows how
Aristotle defends a similar priority of form over matter: “Some identify
the nature or substance of a natural object with the immediate
constituent… e.g., wood is the ‘nature’ of the bed… [others] that
‘nature’ is the shape or form.”[@fink 216, quoting from
@aristotlephysics 2, 1 (192b7ff)] Fink’s comment is:

> Like in Plato, we find here both a definition of the word ‘nature’ (an
> inner source or cause of being moved and being at rest) and two
> competing conceptions of what that source is, namely matter and form
> (the material and the formal cause in Aristotle’s sense). Aristotle
> himself finds it most satisfying to regard the formal (and the
> teleological or final) cause as the nature of x.[@fink 216]

If soul is the primary sense of nature, then body is “second nature.”
Mind (art, intelligence, reason) is the paradigmatic, primary thing
against which mere body is contrasted. A final quotation from Fink puts
the stakes clearly:

> The Athenian doesn’t just leave the concept physis to the ‘men of
> science’. He does not first accept their conception of nature and then
> confront them with the claim that there is something extra-natural –
> the soul or the gods – which they have disregarded and which is in
> fact prior to nature. No. Like McDowell the Athenian is eager to have
> nature on his side. He therefore challenges the scientists’ right to
> restrict the term ‘nature’ to the soulless, partly necessary and
> partly accidental combinations of the elements.[@fink 214]

Fink’s distinction between unrestricted and restricted conceptions of
nature illuminates a surprising fact about the ideological struggle
between bald naturalism and non-naturalistic idealism: both are forms of
restricted naturalism. Classical materialism (bald naturalism) is one
paradigmatic form of naturalism. But the idealist, too, can rightly lay
claim to the title of naturalism – and not in a “Pickwickian” sense.
Whatever one holds to be the “inner source or cause” of a thing, the
immediate constituent matter or the shape, one is a ‘naturalist.’ Each
account lays claim to the title ‘naturalism’ and impugns its rival as
‘non-naturalistic.’

McDowell I think rightly sees that bald naturalistic materialism and
non-naturalistic idealism merely presume their preferred conception of
restricted nature and accuse the other side of ‘non-naturalism.’ For
example, some restricted naturalists simply beg the question against
idealism by defining nature as a material, spatio-temporal, causal
system studied by natural scientific methods. Other restricted
naturalists beg the question against materialism by defining nature as
the formal, immaterial, ideal order studied by rational or practical
methods. My point is not to defend either one but to suggest that
logical consistency demands we choose one or the other restricted
conception of nature (or else resort to the unrestricted conception).

We can now more exactly pose the challenge to McDowell’s account: is he
employing an unrestricted conception of nature or a restricted one? If a
restricted conception of nature, which? On one hand, McDowell rejects
the restricted conception of nature offered him by classical
materialism. He variously impugns this cluster of views as bald
naturalism, philistine scientism, naive realism, etc. On the other hand,
he also explicitly rejects the restricted naturalisms of rampant
Platonism or Kantian idealism.[^67] It would seem, then, that he has
selected the unrestricted view of nature by default.

Instead of explicitly embracing the unrestricted conception without
qualification, he puts the ball in one cup and then moves it around to
the other side, pretending the ball was in the other cup all along. He
keeps his conception of nature restricted (anti-platonist,
anti-supernatural) while *calling* it unrestricted (neither idealist nor
physicalist). Like the materialist, he still wants to wield
“non-naturalism” as a rhetorical weapon against some opponents; but like
the idealist, he wants to wield “philistine scientism” as a rhetorical
weapon against others. McDowell claims to deny dualism by employing an
unrestricted conception of nature while fully endorsing a restricted
conception of nature. The McDowellian picture of nature is
simultaneously restricted and unrestricted.

My view, by contrast, is that organisms (including human beings) are
part of the natural order – and that organic norms (including human
norms) are natural. It is clear that, on unrestricted naturalism, this
way of stating things poses no problems. If organisms and organic norms
can exist in the scientific account of the world, then they are
“natural” by definition.

What about the various restricted naturalisms? I think the only position
excluded by my argument is bald naturalism or classical materialism.
Like McDowell, I think the restricted, mechanical conception of nature
is refuted by the existence of practical rational primates like
ourselves. As Fink says, “McDowell has convincingly shown that what
Bernard Williams calls the absolute conception of reality is merely
restricted, bald naturalism ideologically presented as absolute.”[^68]
Unlike McDowell, I think bald naturalism misunderstands all living
organisms. James Barham captures the dualism into which McDowell
unwittingly falls:

> …the philosophical literature tends to work with a scientifically
> outdated image of living things as rigid “machines.” This results in a
> picture in which only human beings (or at most the higher animals) can
> be properly ascribed purposes and agency in the full normative sense.
> From this perspective, we appear to be faced with an unappealing
> choice between eliminating teleology and normativity from our picture
> of nature altogether and understanding these phenomena as they are
> manifested in our own human form of life as floating free from any
> grounding in the natural world.[@barham 1]

I have problemetized the reductive picture of nature as a mathematical
order excluding not only reasoning but fundamental categories such as
organic life in chapter 2. Even on some restricted forms of naturalism,
the best evidence from biology suggests that there are such things as
natural norms. We cannot build a scientific account of any organism
without them. The picture of nature that emerges is one in which the
natural and normative worlds coincide at the level of biological life.
So, as long as the restricted form of naturalism includes both
descriptive facts studied in sciences such as physics and normative
facts studied in sciences like biology, then it would be consistent with
my view.

### Nature/Human Dualism

The inconsistency in McDowell’s account causes other problems. For
example, he falls prey to the very kind of dualism he explicitly aims to
avoid. Namely, despite *calling* exercises of human practical reasoning
(aimed at becoming virtuous and practically wise) “second nature,” it is
clear that he thinks such exercises belong only to human nature, not to
the (first) natural world. The result is a nature/human dualism that
cuts human beings apart from the non-rational (organic) natural world.
As Julia Annas summarizes, non-reductive naturalism risk trivializing
moral or normative facts by relegating them to humans alone:
“Non-naturalistic accounts of ethical terms assume that their function,
prominently their normativity, is something that arises with humans, or
is produced by humans, in a way which owes nothing to the nature which
we share with other living things.”[@annas2005naturalism 12]

What’s worse, McDowell’s unwitting sort of reason/body dualism cuts
human beings down the middle.[^69] For human beings are also animals,
with animal sensations and emotions. If human responsiveness to the
space of reasons is utterly separate from emotional responsiveness, then
we are left to conclude that emotions are irrational while practical
reason is unemotional.

We might express the contrast by saying that McDowell presents human as
*practical rational agents* full stop, where I presented humans as
practical rational *primates*. I suggested in chapter 4 that this error
leads him into the corresponding error of concluding that successful
practical reasoning is virtue as a whole; by contrast, I argued that
practical wisdom is a virtue of practical reasoning, while other virtues
(such as moderation) are virtues of rational practice. McDowell ignores
that even “non-rational” phenomena such as emotions and even the human
body can be made “rational” in two senses: first, one can take these
into account when reasoning about what to do; and secondly, one can
direct one’s body, emotions, and desires toward good ends. Indeed,
forming one’s emotional reactions into rational patterns is necessary
for the acquisition of certain virtues.[Cf. @hursthouse1998virtue,
chapter 5]

The attraction of my view is that one can see one’s own nature as a
practical rational primate in continuity with non-human nature. The
natural human norms inherent in human practical reasoning are of a piece
with the natural non-human norms of all organic life. As Annas said
above, “we find normativity in the realm of living things, plants and
animals, already.” The exercise of practical reasoning is part of the
same natural order as our biological life form and function. That we
practically reason *is* the natural fact that defines our life form and
what we practically reason *about* are the natural facts that already
obtain for human beings. Chris Toner argues that, on this view, “the
virtues are seen as acquired traits that fit human beings for the
exercise of practical rationality toward which their shared nature
directs them (thereby rejecting McDowell’s sharp separation of first and
second natures).”[@toner2008sorts 243] Toner explains why this view is
more adequate:

> The acquisition of the virtues not only prevents emotions from
> interfering with practical reasoning but also, in McDowellian terms,
> “opens our eyes” to new sorts of reasons for action, not visible to
> the immature, that make the good of others part of our
> good.[@toner2008sorts 243]

In chapter 5, I endorsed McDowell’s view that part of successful
practical reasoning is the initial perceptual sensitivity to certain
facts about what is required. However, the facts to which the virtuous
person becomes sensitive are not a sui generis set of “second natural”
facts but the same natural facts that animals are sensitive to without
reflection. By allowing normativity into our picture of nature at the
organic level as a whole, human powers of theoretical and practical
reasoning come to light as the *awareness* of that normativity, rather
than its invention.

### Inside/Outside

As I briefly mentioned in chapter 5, another major disadvantage of
McDowell’s intersubjective anti-anti-realism is an incorrigible
relativism about practical reasoning (and, for that matter, all
reasoning). Despite his allegiance to “modern science,” McDowell rejects
the putative superiority of scientific knowledge over ethical knowledge,
namely, that scientific knowledge is answerable to the world. Rather
than scientific and ethical inquiry being answerable to the facts of the
world, they are partly responsible to the world while ultimately partly
responsible only to ourselves. This position not only renders scientific
knowledge somewhat more shaky than, I presume, he would wish, it leaves
ethical traditions at the mercy of their own ability to rebuild
Neurath’s boat while at sea.

McDowell is clear that even when a practically wise person actualizes
his nature to acquire the moral outlook, any possible examination of
that moral outlook will be done from *within the moral outlook* itself.
The circularity of this inculcation and new second natural faculty is
not accidental to his account. He says that practical wisdom is
responsive to reasons and so becomes a prototype “for the…faculty that
enables us to recognize and create … intelligibility.”[@mcdowell1996mind
79]

By contrast, Foot’s account aligns more closely with the commonsense
commitment to the objective purport of both morality and rationality.
Our efforts to attain practical wisdom are not *merely* answerable to
the shared form of life of the other practical reasoners with whom we
find ourselves in community; they are also answerable to the natural
norms of our own nature.

I believe Rosalind Hursthouse’s account of neo-Aristotelianism falls
prey to the same criticism as that I have leveled against McDowell’s.
Even though she draws heavily on Foot’s work, she seems to vacillate
between McDowell’s and Foot’s naturalisms when she says, “Ethical
naturalism is not to be construed as the attempt to ground ethical
evaluations in a scientific account of human
nature.”[@hursthouse1998virtue especially chapter 10] She claims that
her account is, like McDowell’s, still loosely naturalistic in that it
is based on “human nature” or “second nature.” But then hasn’t she
thereby rejected Footian naturalism? Jennifer Frey also observes:

> On this issue, Hursthouse seems to be speaking out of both sides of
> her mouth. She wants to acknowledge to Aristotelian critics like John
> McDowell that naturalistic considerations do not convince anyone to
> change their basic moral beliefs or motivate them to action. But at
> the same time, she thinks that she can approach the Humean or the
> Kantian and argue for “the rational credentials” of our moral beliefs
> based upon a “scientific” and “objective” naturalistic account. It is
> unclear how she is supposed to satisfy both parties at once, and the
> tension remains unresolved in her own work.[^70]

My view emphatically *does* aim to ground ethical evaluations in a
scientific account of human nature; where I disagree with Hursthouse,
mostly, is that I reject the assumption that “scientific” has to mean
“non-normative.”

My conception of nature retains a distinction between human beings (as
practical reasoners aware of normativity) and the rest of organic nature
(which is normative but doesn’t know it). The fundamental distinction to
be made is not between rational and non-rational natural entities, but
between living and non-living entities, where humankind shares with
other living species a distinctive set of rational potentialities that
constitute natural normativity. To paraphrase Thomas Nagel, the
existence of objective value is coextensive and co-terminal with the
existence of living things.[@nagel2012mind 117.] I think the common term
‘objective value’ is an unfortunate way to express the notion of natural
normativity. My preferred expression is ‘natural norms.’ Natural norms
such as natural ends exist in all organic life. Natural norms are, for
us, practical reasons. The question is not how human beings perceive or
create “value” but why they act at all. Put this way, it is clear that
every sufficiently matured human organism naturally has reasons to
pursue some ends and to avoid other ends. My picture of nature is one in
which the class of natural facts includes both descriptive facts and
such natural norms.

The corresponding picture of reasoning and knowledge underscores why the
irrelevance problem (mentioned above) is not a problem for my view. The
reason McDowell saw natural norms as irrelevant to practical reasoning
is that he simultaneously endorsed bald naturalism (about organisms) and
social naturalism (about humans). This dualism makes the practical,
normative dimension of nature appear detached from the theoretical,
descriptive dimension, when they are more adequately understood as
dimensions of one and the same world. Jennifer Frey says:

> …the ethical naturalist must be able to show how … these two seemingly
> different senses of good (the good we can derive from an account of
> what simply is and the good as practical goal) can be unified into one
> and the same account. That is, we need an account of natural
> normativity that will show us how the relation between a general
> judgment articulating some fact about a life form (a judgment about a
> fact that is potentially known from the outside) and a judgment
> concerning a particular bearer of that form in a particular situation,
> can take the form of a practical inference whose conclusion is an
> action that exemplifies that very same form of life.[@frey 65]

The Footian solution is to insist that the two forms of judgment are
different ways of apprehending the same fact. The zoo keeper can
apprehend the life form of a sloth bear only “externally”; and the sloth
bear, not being endowed with logos, cannot apprehend its own life form
internally. When it comes to human beings, we can apprehend both ways.
For example, a rational alien who did not share our life form could only
apprehend the life form (practical rational primates) externally just as
scientists can apprehend our life form externally. But a rational human
being can *also* apprehend the selfsame life form “internally” by
reflecting on who and what we are. The facts do not change when we
alternate between the two points of view. Since practical reasoning
*does* contribute to the process of deciding on a course of action, we
can see how norms which are perceived as objective and external become
recognized as relevant and binding.

If both practical and theoretical forms of knowledge grasp the same
object, then the putative opposition between natural facts and practical
reasons is dissolved. General judgments about a life form unite with
practical inferences that are to be acted upon. Scientific reasoning
includes both the external, descriptive point of view and the internal,
normative point of view. Or rather, the normative point of view simply
is one of the scientific points of view. Theoretical reasoning and
practical reasoning are both, broadly, scientific.[^71] Despite
McDowell’s concession to bald naturalism that the modern scientific
picture excludes the space of reasons, on my account, natural scientific
reasoning is no less evaluative than any other expression of reasoning.
Hence, the scientific worldview is capacious enough to include practical
primates and all that they reason about: chemicals, quarks, mathematical
models, biological life forms, or functions. Natural, organic norms
(including those of human beings) are part of the modern scientific
worldview.

Conclusion
----------

This chapter laid out four requirements that the neo-Aristotelian must
meet. I critiqued McDowell’s recourse to a distinction between “first”
and “second nature” which does not explain but mystifies the place of
human norms within the natural order. By contrast, I defended the
Footian alternative which illuminates human norms as instances of
natural norms obtaining in all organisms. If we take an unrestricted
view of nature that absorbs the aesthetic, the ethical, the logical and
so on, then it is merely tautologous to call it ‘natural’ when human
beings engage in normative practical reasoning and reason about
normativity. But even if we take a restricted view of nature to exclude
*some* sorts of entities as non-natural, the kind of natural normativity
that includes human practical reasoning should be included as natural.
Since human beings are natural organisms, and practical reasoning is
natural to our life form, practical reasoning is natural reasoning.

If I were pressed to coin a new term to describe my Footian organic
naturalism, I would call it “recursive naturalism.” Nature “recurs”
within itself. Defining human beings as practical rational primates
entails that we are the one natural organism who reasons about natural
organisms. We can observe the pattern of recursion in each element of
the argument: Humans engage in natural reasoning about all sorts of
things, including natural reasoning itself. We practically reason about
practical reasoning. One of our (basic) natural functions is to discover
(in greater detail) what our natural function is. Having a virtue (in
part) enables us to become more virtuous. Being practically wise enables
us to discern when and how to pursue more practical wisdom.

Conclusion
==========

\setlength{\epigraphwidth}{.95\textwidth}
\begin{epigraphs}
\qitem{Not everything that is last claims to be an end, but only that which is best.}%
{---\textsc{Aristotle, \begin{em}Physics\end{em} 194a.}}
\centering
\end{epigraphs}
In this chapter, I briefly take stock of the main argument of this
dissertation before examining its broader significance and noting a few
connections to other philosophical problems.

The main argument of this dissertation has been that human beings are
best understood as practical, rational primates whose natural ends
include the acquisition of the traditional list of virtues and
(especially) practical wisdom. Since we are by nature practical
reasoning animals, we have a natural obligation to acquire practical
wisdom and any other trait that the practically wise person has.

In outline, I defended this argument by first laying the metanormative
foundation in chapter 2. I developed a novel case for the Footian view I
have labeled ‘organic naturalism.’ In chapter 3, building on this
foundation, I made explicit some of the natural norms that pertain to
human organisms. I argued that our best understanding – if only partial
understanding – of our life form can be expressed in the same sort of
normative/descriptive generics by which biologists and other scientists
identify the life forms of any organism. In chapter 4, I then showed how
the traditional concept of virtue in the Aristotelian tradition falls
under the description of ‘natural human norms’: the virtuous person is
the person described in generic statements such as ‘human beings are
courageous and wise’ etc. Virtues are those practices that are
beneficial to creatures like us, and that are acquirable under the
management of excellent practical reasoning. Virtue and practical wisdom
enable us to actuate our life life form and become what we are. In
chapter 5, I returned to the theme of practical reasoning to show how
the process is best understood as necessarily involving substantive
commitments to pursue good and avoid evil. Some of the mundane facts of
nature are, for us, practical reasons that can motivate us to live a
certain kind of life. Evaluative mistakes are certainly possible, but my
account showed how such mistakes are failures in the attempt to be
practically wise. Chapter 6 attempted to rebut the dual charges of bald
naturalism and non-naturalism by breaking down the putative contrast
between scientific reasoning (about nature) and ethical, practical
reasoning (about norms). I suggested that there is indeed a proper
distinction between theoretical reasoning (whether scientific or
ethical) and practical reasoning (whether scientific or ethical). But
the hard line is not between normative and non-normative reasoning, for
all reasoning is normative in the relevant respects.

The primary criticism of my sort of Footian naturalism, expressed in
various forms by dozens of writers, is that nature (defined in terms of
what the sciences study) and science (defined as the study of nature)
are fundamentally different from norms, reasons, and ethics. In an
effort to dismantle what I take to be an unreflective prejudice, I
criticized the picture of organic nature as merely bald or
non-normative. On both the unrestricted picture of nature and my version
of the restricted conception, norms come to light as natural. I offered
‘recursive naturalism’ as a name for my view. On recursive naturalism,
parts of nature recur within nature: natural organisms (namely, humans)
reason about natural organisms; humans reason about humans; practical
reasoners think about practical reasoning. Rather than shying away from
our best scientific picture of the world – including biological and
human phenomena – recursive naturalism whole-heartedly embraces that
picture. Indeed, affirming recursive naturalism makes it possible to
affirm both moral and scientific realism; denying recursive naturalism
seems to require denying both moral realism and scientific realism.

My account cannot pretend to have addressed every incisive objection or
to have covered every crucial topic. I have aimed my argument,
throughout, at the scientific naturalist who is in some sense already
committed to scientific realism. Hence, I have attempted to clarify how
my Footian sort of ethical naturalism can be compatible with a plausible
version of scientific naturalism. But one possible shortcoming is the
quick manner with which I have had to deal with delicate matters of
epistemology and (especially) the philosophy of science. Scientific
realism is by no means the only reasonable view, and there are many
brands of scientific realism.

Another possible shortcoming is the absence of a discussion about the
relation between virtue ethics and religious morality. Virtue ethics is
often associated with Christian, Muslim, Jewish, or Taoist religious
philosophy. Nevertheless, I have defended (especially) Foot’s version of
what Murphy calls a “secular natural law theory.” Foot, McDowell and
others are non-religious philosophers who find in Aristotle an
alternative that is neutral with respect to theism. My hope is to play
some part in showing the plausibility and practicality of the notion
that even “modern knowers and godless anti-metaphysicians” have every
reason to pursue virtue and wisdom.[^72]

A third possible shortcoming is a fuller discussion of social reasoning.
While ‘homo sapiens sapiens’ is a biological concept that purports to
range over all genetically modern humans, the variety and contrast
between the ways various cultures conceive of and pursue ‘the good life
for humans’ is daunting. If, as MacIntyre has argued, we learn to reason
within a social tradition, the problem of cultural relativism about
rationality looms large. A fuller discussion would have to engage
thoroughly with recent anthropological and sociobiological literature.

In spite of these admitted shortcomings, my project has been to
establish that human beings indeed have natural ends, such as the
acquisition of virtue and practical wisdom. Neo-Aristotelian ethical
naturalism can provide mutually reinforcing accounts of individual
concepts such as virtue, practical reason, nature and human nature. When
viewed together, these concepts form an interlocking whole that has the
potential to solve problems in both ethics and metaethics, and beyond.
The attractions of this view are manifold.

First, it is always dangerous to do moral philosophy *without*
considering the theories of other times, places, and cultures, for we
are liable to overemphasize pet virtues (or ignore pet vices) peculiar
to our time and place. Neo-Aristotelianism draws on the ethical writings
of other cultures and other times and so promises to correct lopsided
ethical developments in our own time.

Secondly, neo-Aristotelian ethical naturalism provides a satisfying
possible answer to the problem of the relation between nature and
reason. It pictures facts and norms as an organic whole, presented to us
by the world and studied by all the sciences, including formal or
abstract sciences. It even suggests that Aristotle was right to classify
ethics as a different sort of science with its own subject matter, its
own standards, and its own aims.[^73]

Neither subsuming ethics under (merely descriptive) disciplines nor
subsuming descriptive disciplines into normative categories,
neo-Aristotelian theory holds great promise for coordinating the
descriptive and normative dimensions of ethics, biology, and other
sciences. Perhaps this is part of the explanation why the Footian sort
of neo-Aristotelian virtue ethics is rightly enjoying a renaissance in
contemporary analytic ethics and beyond. In my view, it is both
perfectly compatible with the modern scientific worldview and also
useful in political life, bioethics,[@beauchamp2001principles]
business,[@beadle2015macintyre] education,[@carr2005virtue] and everyday
life. It would be an improvement to almost any area of human life if we
were aware of our own vices and worked to expunge them, and if we
understood the virtues and pursued them.

Virtue, practical reason, and nature are age-old themes which demand
more work than I can claim to have done here adequately. As Glaucon said
to Socrates, “The measure of listening to such discussions is the whole
of life.”[@plato, *Republic* 450b.]

\backmatter

Bibliography
============

\thispagestyle{plain}

**Bibliography**

Andreou, Chrisoula. “Getting on in a Varied World.” *Social Theory and
Practice*, vol.32, no. 1 (2006): 61–73.

Annas, Julia. “Being Virtuous and Doing the Right Thing.” In
*Proceedings and Addresses of the American Philosophical Association*,
61–75, 2004.

———. *Intelligent Virtue*. Oxford University Press, 2011.

———. *The Morality of Happiness*. Oxford University Press, 1993.

———. “Virtue Ethics and the Charge of Egoism.” In *Morality and Self
Interest*, edited by Paul Bloomfield, 205–21. Oxford University Press,
2009.

———. “Virtue Ethics: What Kind of Naturalism?” In *Virtue Ethics, Old
and New*, edited by Stephen Gardiner, 11–29. Cornell University Press,
2005.

Anscombe, Elizabeth. “Modern Moral Philosophy.” *Philosophy* 33, no. 124
(1958): 1–19.

Aquinas, Thomas. *Summa Theologiae.*

Arnhart, Larry. “Aristotle’s Biopolitics: A Defense of Biological
Teleology against Biological Nihilism.” *Politics and the Life Sciences*
6, no. 2 (1988): pp. 173–229.

———. “The New Darwinian Naturalism in Political Theory.” *American
Political Science Review* 89, no. 02 (1995): 389–400.

Barham, James. “Teleological Realism in Biology.” PhD thesis, University
of Notre Dame, 2011.

Bailey, Andrew M. “Animalism.” *Philosophy Compass* 10, no. 12 (2015):
867–83.

\thispagestyle{plain}

Beadle, Ron. “MacIntyre’s Influence on Business Ethics.” In *Handbook of
Virtue Ethics in Business and Management*, 1–9. Springer, Dordrecht,
2015.

Beauchamp, Tom, and James Childress. *Principles of Biomedical Ethics*.
Oxford University Press, 2001.

Blackburn, Simon. *Spreading the Word*. Oxford University Press, 1985.

Blackman, Reid D. “Meta-Ethical Realism with Good of a Kind.” \_European
Journal of Philosophy, \_Vol. 23, no. 2 (2015): 273–92.

Blair, James, Derek Mitchell, and Karina Blair. *The Psychopath: Emotion
and the Brain.* Blackwell Publishing, 2005.

Bloomfield, Paul. “Eudaimonia and Practical Rationality.” In *Virtue and
Happiness*, edited by Rachana Kamtekar. Oxford University Press, 2012.

Bostrom, Nick. “In Defense of Posthuman Dignity.” *Bioethics* 19, no. 3
(2005): 202–14.

———. “Transhumanist Values.” *Journal of Philosophical Research* 30
(2005): 3–14.

Boyd, Richard. “Finite Beings, Finite Goods: The Semantics, Metaphysics
and Ethics of Naturalist Consequentialism.” *Philosophy and
Phenomenological Research* 66, no. 3 (2003): 505–53.

———. “How to Be a Moral Realist.” *Contemporary Materialism*, 1988, 307.

———. “Realism, Anti-Foundationalism and the Enthusiasm for Natural
Kinds.” *Philosophical Studies* 61, no. 1 (1991): 127–48.

Brown, R. Stephen. *Moral Virtue and Nature: A Defense of Ethical
Naturalism*. Continuum, 2008.

Brown, Stephen. “Really Naturalizing Virtue.” *Ethica* 4 (2005): 7–22.

Carlson, Greg N. “A Unified Analysis of the English Bare Plural.”
*Linguistics and Philosophy* 1, no. 3 (1977): 413–57.

Carr, David, and Jan Steutel. *Virtue Ethics and Moral Education*.
Routledge, 2005.

Cimpian, Andrei, Amanda C Brandone, and Susan A Gelman. “Generic
Statements Require Little Evidence for Acceptance but Have Powerful
Implications.” *Cognitive Science* 34, no. 8 (2010): 1452–82.

\thispagestyle{plain}

Cohen, Ariel. “On the Generic Use of Indefinite Singulars.” *Journal of
Semantics* 18, no. 3 (2001): 183–209.

Cohn, Jeffrey P. “Saving the California Condor.” *BioScience* 49, no. 11
(1999): 864–68.

Cooper, John. *Complete Works of Plato*. Hackett, 1997.

Cummins, Robert. “Functional Analysis.” *The Journal of Philosophy* 72,
no. 20 (1975): 741–65.

Cuneo, Terence. *Speech and Morality*. Oxford University Press, 2014.

———. *The Normative Web*. Oxford University Press, 2007.

D’Andrea, Thomas D. *Tradition, Rationality, and Virtue: The Thought of
Alasdair MacIntyre*. Ashgate Publishing, Ltd., 2006.

Deacon, Terrence W. *The Symbolic Species: The Co-Evolution of Language
and the Brain*. WW Norton & Company, 1998.

Dupré, John. *Processes of Life: Essays in the Philosophy of Biology*.
Oxford University Press, 2012.

Edgley, Roy. “Practical Reason.” *Mind*, 74, no. 294 (1965): 174–91.

FitzPatrick, William. “Morality and Evolutionary Biology.” In *The
Stanford Encyclopedia of Philosophy*, edited by Edward N. Zalta, Spring
2016., 2016.

Flew, Antony. *Thinking about Thinking: Or, Do I Sincerely Want to Be
Right?* Fontana/Collins, 1975.

Fodor, Jerry A. *The Mind Doesn’t Work That Way: The Scope and Limits of
Computational Psychology*. MIT press, 2001.

Foot, Philippa. “Does Moral Subjectivism Rest on a Mistake?” *Royal
Institute of Philosophy Supplement* 46 (2000): 107–23.

———. *Natural Goodness*. Oxford University Press, 2001.

———. *Virtues and Vices: And Other Essays in Moral Philosophy*. Oxford
University Press, 2002.

Frankena, William K. “The Naturalistic Fallacy.” *Mind*, 1939, 464–77.

Frey, Jennifer Ann. “The Will and the Good.” University of Pittsburgh,
2012.

Gelman, Susan, and Lawrence Hirschfeld. “How Biological Is
Essentialism.” *Folkbiology* 9 (1999): 403–46.

Gibbard, Allan. “Normative Properties.” *The Southern Journal of
Philosophy* 41, no. S1 (2003): 141–57.

\thispagestyle{plain}

———. *Thinking How to Live*. Harvard University Press, 2009.

———. *Wise Choices, Apt Feelings: A Theory of Normative Judgment*.
Harvard University Press, 1992.

Godfrey-Smith, Peter. “Conditions for Evolution by Natural Selection.”
*The Journal of Philosophy* 104, no. 10 (2007): 489–516.

Goodall, Jane. “Infant Killing and Cannibalism in Free-Living
Chimpanzees.” *Folia Primatologica* 28, no. 4 (1977): 259–82.

Haldane, John. “A Return to Form in the Philosophy of Mind.” *Ratio* 11,
no. 3 (1998): 253–77.

———. “On Coming Home to (Metaphysical) Realism.” *Philosophy* 71, no.
276 (1996): 287–96.

Harmon, Justin L. “The Normative Architecture of Reality: Towards an
Object-Oriented Ethics.” PhD Dissertation, University of Kentucky, 2013.

Heath, Dwight B. “Sociocultural Variants in Alcoholism.” *Encyclopedic
Handbook of Alcoholism*, 1982, 426–40.

Hooker, Brad, and Bart Streumer. “Procedural and Substantive Practical
Rationality.” In *The Oxford Handbook of Rationality*, 57–74. Oxford
University Press, 2004.

Horn, Laurence R. “Contradiction.” In *The Stanford Encyclopedia of
Philosophy*, edited by Edward N. Zalta, Spring 2014., 2014.

Horton, John, and Susan Mendus. *After MacIntyre: Critical Perspectives
on the Work of Alasdair MacIntyre*. University of Notre Dame, 1994.

———. “Alasdair MacIntyre: After Virtue and After.” In *Current
Controversies in Virtue Theory*, edited by Mark Alfano. Routledge, 2015.

Huang, Yong. “The Self-Centeredness Objection to Virtue Ethics.”
*American Catholic Philosophical Quarterly* 84, no. 4 (2010): 651–92.

Huneman, Philippe. “Naturalising Purpose: From Comparative Anatomy to
the \`adventure of Reason’.” *Studies in History and Philosophy of
Science Part C: Studies in History and Philosophy of Biological and
Biomedical Sciences* 37, no. 4 (2006): 649–74.

\thispagestyle{plain}

Hurka, Thomas. *Virtue, Vice, and Value*. Oxford University Press, 2000.

Hursthouse, Rosalind. “Normative Virtue Ethics.” In *How Should One
Live?: Essays on the Virtues*, edited by Roger Crisp, 19–33. Oxford
University Press, 1996.

———. *On Virtue Ethics*. Oxford University Press, 1998.

———. “Virtue Ethics and Human Nature.” *Hume Studies* 25, no. 1 (1999):
67–82.

———. “Practical Wisdom: A Mundane Account.” In *Proceedings of the
Aristotelian Society*, 106:283–307. Wiley-Blackwell, 2006.

———. “Neo-Aristotelian Ethical Naturalism.” *The International
Encyclopedia of Ethics*, 2013.

———. “Virtue Ethics.” In *The Stanford Encyclopedia of Philosophy*,
edited by Edward N. Zalta, 2013.

Jin, Xiangshu, Robert Townley, and Lawrence Shapiro. “Structural Insight
into AMPK Regulation: ADP Comes into Play.” *Structure* 15, no. 10
(2007): 1285–95.

Johnson, Monte. *Aristotle on Teleology*. Oxford University Press, 2005.

Krifka, Manfred. “Bare NPs: Kind-Referring, Indefinites, Both, or
Neither?” In *Semantics and Linguistic Theory*, 13:180–203, 2003.

Kripke, Saul A. *Wittgenstein on Rules and Private Language: An
Elementary Exposition*. Harvard University Press, 1982.

Lawson, Christine Ann. *Understanding the Borderline Mother*. Jason
Aronson, Incorporated, 2000.

Lenman, James. “Moral Naturalism.” In *The Stanford Encyclopedia of
Philosophy*, edited by Edward N. Zalta, 2014.

Lennox, James. “Teleology.” *Keywords in Evolutionary Biology*, Harvard
University Press, 1992: 324–33.

———. “Darwin Was a Teleologist.” *Biology and Philosophy* 8, no. 4
(1993): 409–21.

Leslie, John. “The Theory That the World Exists Because It Should.”
*American Philosophical Quarterly* 7, no. 4 (1970): 286–98.

Leslie, Sarah-Jane. “Generics: Cognition and Acquisition.”
*Philosophical Review* 117, no. 1 (2008): 1–47.

\thispagestyle{plain}

Leunissen, Mariska. *Explanation and Teleology in Aristotle’s Science of
Nature*. Cambridge University Press, 2010.

Levy, Sanford. “Philippa Foot’s Theory of Natural Goodness.” In *Forum
Philosophicum*, 14:1–15, 2009.

Linquist, Stefan, Edouard Machery, Paul E Griffiths, and Karola Stotz.
“Exploring the Folkbiological Conception of Human Nature.”
*Philosophical Transactions of the Royal Society of London B: Biological
Sciences* 366, no. 1563 (2011): 444–53.

Lott, Micah. “Moral Virtue as Knowledge of Human Form.” *Social Theory
and Practice* 38, no. 3 (2012): 407–31.

Lutz, Christopher. *Tradition in the Ethics of Alasdair MacIntyre*.
Lexington Books, 2004.

———. *Reading Alasdair MacIntyre’s After Virtue*. A&C Black, 2012.

———. “Alasdair MacIntyre.”*Internet Encyclopedia of Philosophy*, 2015.
Web. http://www.iep.utm.edu/mac-over/

MacFarquhar, Larissa. *Strangers Drowning: Grappling with Impossible
Idealism, Drastic Choices, and the Overpowering Urge to Help*. Penguin
Press HC, 2015.

MacIntyre, Alasdair. “Hume on Is and Ought.” *The Philosophical Review*,
1959, 451–68.

———. “Social Science Methodology as the Ideology of Bureaucratic
Authority,” in *Through the Looking Glass: Epistemology and the Conduct
of Inquiry*, Maria J. Falco, ed. (Washington: University Press of
America, 1979) pp. 42-58. Reprinted in Kelvin Knight, ed. *The MacIntyre
Reader.* pp. 53-68.

———. *After Virtue*. University of Notre Dame, 1984.

———. “Does Applied Ethics Rest on a Mistake?” *The Monist* 67, no. 4
(1984): 498–513.

———. “The Relationship of Philosophy to Its Past.” *Philosophy in
History*, 1984, 31–48.

———. “Relativism, Power and Philosophy.” In *Proceedings and Addresses
of the American Philosophical Association*, 5–22. 1985.

———. “The Idea of an Educated Public.” *Education and Values: The
Richard Peters Lectures* 15 (1987).

———. *Whose Justice? Which Rationality?* University of Notre Dame, 1988.

———. *Three Rival Versions of Moral Enquiry*. University of Notre Dame,
1990.

\thispagestyle{plain}

———. *Macintyre Reader*. Edited by Kelvin Knight. University of Notre
Dame, 1998.

———. *Dependent Rational Animals: Why Human Beings Need the Virtues*.
Cambridge University Press, 1999.

———. “Virtues in Foot and Geach.” *Philosophical Quarterly*, no. 52
(2002): 621–31.

Mautner, Michael. “Life-Centered Ethics, and the Human Future in Space.”
*Bioethics* vol. 23, no. 8 (2009): 433–40.

Mayr, Ernst. “The Idea of Teleology.” *Journal of the History of Ideas*
53, no. 1 (1992): pp. 117–35.

McDowell, John. “Virtue and Reason.” *The Monist* 62, no. 3 (1979):
331–50.

———. “The Role of Eudaimonia in Aristotle’s Ethics’.” In *Essays on
Aristotle’s Ethics*, edited by Amélie Oksenberg Rorty, 359–76.
University of California Press, 1980.

———. *Mind and World*. Harvard University Press, 1996.

———. *Mind, Value, and Reality*. Harvard University Press, 1998.

———. “Two Sorts of Naturalism.” In *Mind, Value, and Reality*, 167–97.
Harvard University Press, 1998.

———. “Values and Secondary Qualities.” In *Mind, Value, and Reality*,
131–50. Harvard University Press, 1998.

———. “Naturalism in the Philosophy of Mind.” In *Naturalism in
Question*, edited by Mario De Caro and David Macarthur, 91–105. Harvard
University Press, 2004.

McDowell, John, and I. G. McFetridge. “Are Moral Requirements
Hypothetical Imperatives?” *Proceedings of the Aristotelian Society,
Supplementary Volumes* 52 (1978): 13–42.

Melville, Herman. *Bartleby, the Scrivener*. Best Classic Books,1966.

Millgram, Elijah. “Reasonably Virtuous.”  In \_Ethics Done Right:
Practical Reasoning as a Foundation for Moral Theory. \_Cambridge
University Press, 2005.

Millikan, Ruth Garrett.“In Defense of Proper Functions.” *Philosophy of
Science*, 56, No. 2 (1989): 288–302.

—. *Language, Thought, and Other Biological Categories: New Foundations
for Realism*. MIT press, 1984.

\thispagestyle{plain}

Morell, Virginia. “Why Do Animals Sometimes Kill Their Babies?”
*National Geographic*, 2014.
[http://news.nationalgeographic.com/news/](http://news.nationalgeographic.com/news/2014/03/140328-sloth-bear-zoo-infanticide-chimps-bonobos-animals/).

Murphy, Mark. “The Natural Law Tradition in Ethics.” In *The Stanford
Encyclopedia of Philosophy*, edited by Edward N. Zalta, 2011.

Murphy, Mark C. *Alasdair MacIntyre*. Cambridge University Press, 2003.

Nagel, Thomas. *The Possibility of Altruism*. Princeton University
Press, 1978.

———. *The View from Nowhere*. Oxford University Press, 1989.

———. *Mind and Cosmos*. Oxford University Press, 2012.

Nussbaum, Martha. “Aristotle on Human Nature and the Foundations of
Ethics.” In *World, Mind, and Ethics: Essays on the Ethical Philosophy
of Bernard Williams*, edited by J.E.J. Altham and Ross Harrison, 86–131.
Cambridge University Press, 1995.

———. “Non-Relative Virtues: An Aristotelian Approach.” *Midwest Studies
In Philosophy* 13, no. 1 (1988): 32–53.

———. “Virtue Ethics: A Misleading Category?” *The Journal of Ethics* 3,
no. 3 (1999): 163–201.

Oakes, Edward. “The Achievement of Alasdair Macintyre.” *First Things*,
1996.

Pelletier, Francis Jeffry, and Greg N Carlson. *The Generic Book*.
University of Chicago Press, 1995.

Perlman, Mark. “The Modern Philosophical Resurrection of Teleology.”
*The Monist* 87, no. 1 (2004): 3–51.

Pincoffs, Edmund. “Quandary Ethics.” *Mind*, 1971, 552–71.

Pinker, Steven. *The Blank Slate: The Modern Denial of Human Nature*.
Penguin, 2003.

Pittendridgh, Colin. “Adaptation, Natural Selection, and Behavior” in
*Behavior and Evolution.* Anne Roe and George Gaylord Simpsons (eds.).
New Haven, 1958.

Plantinga, Alvin. *Where the Conflict Really Lies: Science, Religion,
and Naturalism*. Oxford University Press, 2011.

\thispagestyle{plain}

Prasada, Sandeep, Sangeet Khemlani, Sarah-Jane Leslie, and Sam
Glucksberg. “Conceptual Distinctions amongst Generics.” *Cognition* 126,
no. 3 (2013): 405–22.

Quinn, Warren. “Rationality and the Human Good.” *Social Philosophy and
Policy* 9, no. 02 (1992): 81–95.

\thispagestyle{plain}

Quinn, Warren, and Philippa Foot. *Morality and Action*. Cambridge
University Press, 1993.

Railton, Peter. “Moral Realism.” *Philosophical Review* 95, no. 2
(1986).

Rehg, William, and Darin Davis. “Conceptual Gerrymandering? The
Alignment of Hursthouse’s Naturalistic Virtue Ethics with Neo-Kantian
Non-Naturalism.” *The Southern Journal of Philosophy* 41, no. 4 (2003):
583–600.

Russell, Bertrand. *The Basic Writings of Bertrand Russell, 1903-1959*.
Psychology Press, 1992.

Sadler, Brook J. “Review of ‘Natural Goodness.’” *Essays in Philosophy*
5, no. 2 (2004): 28.

Sartre, Jean-Paul. *Being and Nothingness*. Open Road Media, 2012.

Shafer-Landau, Russ. *Moral Realism: A Defense*. 4. Oxford University
Press, 2003.

Shapiro, James A. “Revisiting the Central Dogma in the 21st Century.”
*Annals of the New York Academy of Sciences* 1178, no. 1 (2009): 6–28.

Slote, Michael. “Agent-Based Virtue Ethics.” *Midwest Studies in
Philosophy* 20, no. 1 (1995): 83–101.

———. *From Morality to Virtue*. Oxford University Press, 1992.

Taylor, Charles. “Justice After Virtue.” In *After MacIntyre*, 16–43.
University of Notre Dame, 1994.

Thompson, Allen. “Reconciling Themes in Neo-Aristotelian Meta-Ethics.”
*The Journal of Value Inquiry* 41, no. 2 (2007): 245–63.

Thompson, Michael. “Apprehending Human Form.” *Royal Institute of
Philosophy Supplement* 54 (2004): 47–74.

———. *Life and Action*. Harvard University Press, 2008.

———. “The Representation of Life.” In *Virtues and Reasons*, edited by
Gavin Rosalind, Lawrence Hursthouse and Warren Quinn, 247–96. Oxford:
Clarendon Press, 1995.

Toner, Christopher. “Flourishing and Self-Interest in Virtue Ethics.”
PhD Dissertation, University of Notre Dame, 2003.

\thispagestyle{plain}

———. “Sorts of Naturalism: Requirements for a Successful Theory.
*Metaphilosophy*, 39 (2):220–250, 2008.

Waddington, Conrad Hal, and others. *The Strategy of the Genes. A
Discussion of Some Aspects of Theoretical Biology.* George Allen &
Unwin, Ltd., 1957.

Waismann, Friedrich. *How I See Philosophy*. Springer, 1968.

Wallace, R. Jay. “Practical Reason.” In *The Stanford Encyclopedia of
Philosophy*, edited by Edward N. Zalta, 2014.

Ward, Arthur. “Against Natural Teleology and Its Application in Ethical
Theory.” Bowling Green State University, 2013.

Ward, Keith. “Kant’s Teleological Ethics.” *The Philosophical Quarterly*
21, no. 85 (1971): 337–51.

Weaver, Richard M. *The Ethics of Rhetoric*. Psychology Press, 1985.

Weinstein, Jack Russell. *On MacIntyre*. Wadsworth, 2003.

Wielenberg, Erik. “The Nature of Moral Virtue.” PhD Dissertation, 2000.

Wiggins, David. “Deliberation and Practical Reason.” *Proceedings of the
Aristotelian Society* 76 (1975): 29–51.

Williams, Bernard. “Internal and External Reasons.” In *Ethical Theory:
An Anthology*, edited by Russ Shafer-Landau, 292–98, 2007.

Wilson, Edward. *Sociobiology: The New Synthesis*. Harvard University
Press, 1978.

Woodcock, Scott. “Philippa Foot’s Virtue Ethics Has an Achilles’ Heel.”
*Dialogue* 45, no. 03 (2006): 445–68.

Zammito, John. “Teleology Then and Now: The Question of Kant’s Relevance
for Contemporary Controversies over Function in Biology.” *Studies in
History and Philosophy of Science Part* 37, no. 4 (2006): 748–70.

\thispagestyle{plain}

\newpage

Vita
====

\begin{center}
\LARGE
Vita
\normalsize

Keith Buhler

Department of Philosophy   

University of Kentucky    

Lexington, KY 40506  

\end{center}
\noindent EDUCATION

1.  M.A.  Philosophy, University of Kentucky, 2014
2.  M.A.  Orthodox Theology, University of Balamand, 2012
3.  B.A.   Humanities, emphasis History, Biola University, 2004

\noindent EMPLOYMENT

1.  Postdoctoral Lecturer, University of Kentucky Spring 2017
2.  Instructor of Philosophy, Asbury University, 2013-2017

\noindent RESEARCH

1.  Specialization: Ethics
2.  Competence: Philosophy of Mind, History of Philosophy, and
    Philosophy of Religion

\noindent  UNIVERSITY TEACHING

1.  Business Ethics (Fall 2016, Spring 2017 UK)
2.  Health Care Ethics (Spring 2015, Fall 2016, UK)
3.  Introduction to Philosophy (2013-2014, UK, 2014-2017 Asbury)
4.  Introduction to Ethics (Fall 2013, UK)
5.  Introduction to Logic (Spring 2013)
6.  Philosophy of Religion (Summer 2016, Asbury)
7.  Philosophy of C.S. Lewis (Fall 2016, Asbury)
8.  Virtue Ethics, Ancient and Modern (Spring 2016, Asbury)
9.  Introduction to Logic (Spring 2013)
10. Introduction to Logic (Fall 2012, UK, under Bob Sandmeyer)
11. Philosophy of Science (summer 2004, Biola University, under Nancy
    Pearcey)

\thispagestyle{plain}

\noindent SECONDARY SCHOOL TEACHING

12. Introduction to Philosophy (online course, Freedom Project Academy,
    2017)
13. Humanities: 20th Century British Thought (Veritas Academy, KY 2013)
14. Philosophy: Plato on Being and Knowing (Torrey Academy, CA 2011)
15. Philosophy: Traditional Logic (Torrey Academy, 2009-2010)
16. Humanities: Foundations of American Thought (Torrey Academy,
    2009-2012)
17. Humanities: Ancient and Medieval Thought (Torrey Academy, 2008-2012)
18. Humanities: 20th Century British Thought (Torrey Academy, 2007-2012)
19. Philosophy: Great Books Tutor, GATE Program (Willow School of Long
    Beach, CA 2001-2002)
20. Spanish Tutor (Torrey Academy, Private Tutoring, 2007-2008)
21. ESL Tutor (Etum Academy, CA 2010-2012)
22. ESL Tutor (Biola University Abroad, Ulaambatar, Mongolia, 2001)

\noindent PRESENTATIONS

1.  “Natural Teleology without Theology in Thomas Nagel’s *Mind and
    Cosmos*” Society of Christian Philosophers, University of San Diego,
    2016.
2.  “Fairy Tale Nihilism: The Empty Hero in *Kung Fu Panda* and *The
    Great and Powerful Oz*,” Faith and Film Conference, Baylor
    University, 2014.
3.  “Is the Cosmos Causally Closed?” Ian Ramsey Centre, Oxford
    University, 2014.
4.  “Socratic Therapy,” SOPHIA Conference, Spring Branch, TX 2014.
5.  “Virtue and Imaginative Resistance,” Midsouth Philosophy Conference,
    Rhodes College, 2014.
6.  “Virtue and Imaginative Resistance,” South Carolina Society of
    Philosophers, University of South Carolina, 2014.

\noindent COMMMENTS AND SERVICE

1.  Comments on David Skowronski’s “Inductive Reasoning in Naturalism
    and Supernaturalism.” Society of Christian Philosophers, University
    of San Diego, 2016.
2.  Session Chair, Ian Ramsey Centre Conference, Oxford University,
    2014.
3.  Comments on Andrew Greenlee’s “Combating the Normativity Challenge
    to Virtue Ethics,” Midsouth Philosophy Conference, Rhodes College,
    2014.
4.  Referee for Kentucky Graduate School Conference submissions, 2013.

\noindent AWARDS AND HONORS

1.  Travel Funding, University of Kentucky Philosophy Department (2014,
    2015, 2016)
2.  Travel Funding, University of Kentucky Graduate School (2014)
3.  Teaching Assistantship, University of Kentucky (2012-2016)\
4.  Perpetual Member of the Torrey Honors Institute, Academic Honors
    Society (2014)

\noindent ADMINISTRATION AND LEADERSHIP

1.  Director of High School Studies (Veritas Academy, 2013-2014)
2.  Master Tutor (Torrey Academy, 2010-2012)
3.  Lecturer (Wheatstone Academy, 2006-2011)
4.  Assistant Director (Wheatstone Academy, 2004-2005)

\thispagestyle{plain}

\noindent INVITED PUBLIC TALKS

1.  “Morality: Rule-following or New Life?,” Wesleyan Society, Lexington
    KY, 2014.
2.  “Reading Great Books in Classical Education,” Veritas Academy,
    Lexington KY, 2013.
3.  “The Goodness of the Tao: CS Lewis’ *Abolition of Man*,” Torrey
    Academy, CA 2012.
4.  “Is Vainglory Pride? Dorothy Sayers’ *Gaudy Night*,” Torrey Academy,
    2012.
5.  “The Philosophy of Pain,” St. Barnabas Church, CA 2011.
6.  “Hope and the Cycle of Desire,” Hope Academy, 2011.
7.  “The Art of Conversation: Conversation with Art,” Wheatstone
    Academy, La Habra, CA 2011.
8.  “Goodness, Truth, and Beauty,” St. George Church, CA 2010.
9.  “The Virtue of Constancy,” Hope Academy, Yorba Linda, CA 2009.
10. “Life Experience as a Text: Learning From Initiatives,” Biola
    University, CA 2007.\newline

\noindent GRADUATE COURSEWORK

\noindent (Professional Development Courses, University of Kentucky)

1.  Proseminar on Teaching Philosophy, David Bradshaw.
2.  Preparing Future Faculty, Morris Grubbs.

(Philosophy Courses, University of Kentucky)

3.  Seminar on Post-Kantian Ethics: Fichte and Hegel on Right. Dan
    Breazeale.
4.  Seminar on Metaethics: Moral Motivation. Anita Superson.
5.  Seminar on Ethics and Bodily Autonomy. Anita Superson.
6.  Seminar on Metaethics: Normative Language. Tim Sundell.
7.  Metaethics (Dissertation residency). David Bradshaw.
8.  Ethical Naturalism (Independent study). David Bradshaw.
9.  MacIntyre and After Virtue (Independent study). David Bradshaw.
10. Ethics from Hobbes to Feminism. Anita Superson.
11. Seminar on Plato’s Forms and the Death of Gods (audit). Eric Sanday
12. Seminar on Plato’s *Philebus* and Timaeus. Eric Sanday.
13. Seminar on Plato’s *Parmenides*. Eric Sanday.
14. Aristotle and Aristotelians on Mind (Independent study). David
    Bradshaw.
15. Ancient Greek Metaphysics. Eric Sanday.
16. Seminar on Mind and Imagination. Clare Batty.
17. Seminar on Kantian Idealism. Stefan Bird-Pollan.
18. Seminar on Metaphysical Naturalism. David Bradshaw.
19. Philosophy of Religion. David Bradshaw.
20. Symbolic Logic. Tim Sundell.

(Taken at Biola University)

21. Philosophy of Mind. JP Moreland.
22. Metaphysics of Substance and Property. JP Moreland.
23. Philosophy of Cosmology and Quantum Physics. John Bloom. \newline

\thispagestyle{plain}

\noindent LANGUAGES

1.  Ancient Greek (proficient)
2.  Spanish (fluent)
3.  HTML, CSS, and LaTex (basic)

\noindent AFFILIATIONS

1.  Society of Medieval and Renaissance Philosophy, 2012-present
2.  American Philosophical Association, 2014-present
3.  Society of Orthodox Philosophers in America, 2014-present
4.  International Society for MacIntyrean Enquiry, 2015-present
5.  National Association of Scholars, 2016-present \newline

\newpage

\thispagestyle{empty}

[^1]: E.g., Hume, *Enquiry Concerning the Principles of Morals*,
    Appendix I.

[^2]: @wilson1975sociobiology 562

[^3]: Jay Wallace explains robust realism as the “idea that there are
    facts of the matter about what we have reason to do that are prior
    to and independent of our deliberations, to which those
    deliberations are ultimately answerable… [such facts constitute] an
    objective body of normative truths. @seppracticalreason, section 2.
    Wallace cites Parfit (2011) and Scanlon (2014).

[^4]: Cornell realists such as Richard Boyd and Nicholas Sturgeon argue
    that moral facts supervene on nonmoral facts in much the same way
    biological facts supervene on physical ones. My dissertation cannot
    enter deeply into discussions with views of this kind, but the
    comparisons and contrasts are important to make. For example, why is
    it that Boyd, Sturgeon and Gibbard are consequentialists in their
    normative theory while neo-Aristotelians are not? I briefly address
    this question in chapter 4. And why do Boyd et al. mostly focus
    their explanations of terms and facts like ‘goodness’ on instances
    of what is good for humans? It will be clear in chapter 2 that I am
    willing to countenance a larger set of normative facts about all
    organic life.

[^5]: @annas2005naturalism

[^6]: James Barham calls his own version of the Footian view “reformed
    naturalism.” (@barham 215.) I shall call my version ‘recursive
    naturalism,’ for reasons I explain in chapter 6.

[^7]: Murdoch assumes that human life has “no external point or τελος,”
    but that it has a point *from within.* @murdoch1998sovereignty 79

[^8]: McDowell calls his view by a variety of names: ‘liberal
    naturalism’ (*Mind and World*, Harvard 1996, 89, 98); ‘acceptable
    naturalism’ (*Mind, Value, and Reality* 197); ‘Greek naturalism’
    (*Mind and World* 174); ‘Aristotelian naturalism’ (*Mind and World*
    196), ‘naturalism of second nature’ (*Mind and World* 86); or
    ‘naturalized platonism’ (*Mind and World* 91). Christopher Toner
    calls McDowell’s view ‘excellence naturalism’ or ‘culturalism.’
    Along the same lines, Goetz and Taliaferro distinguish ‘strict’ and
    ‘relaxed’ versions of naturalism: @goetz2008naturalism. For further
    exploration of these distinctions, see @fink, 204.

[^9]: Cf. Aristotle, *Nicomachean Ethics*, Book II; Hegel, *Elements of
    the Philosophy of Right*, Part III, § 151.

[^10]: Cf. Wilfred Sellars, *Empiricism and the Philosophy of Mind*, §
    36.

[^11]: In a famous passage, Hume says: “In every system of morality,
    which I have hitherto met with, I have always remarked, that the
    author proceeds for some time in the ordinary ways of reasoning, and
    establishes the being of a God, or makes observations concerning
    human affairs; when all of a sudden I am surprised to find, that
    instead of the usual copulations of propositions, is, and is not, I
    meet with no proposition that is not connected with an ought, or an
    ought not. This change is imperceptible; but is however, of the last
    consequence.” (*A Treatise of Human Nature* book III, part I,
    section I.) Nevertheless, Arnhart and MacIntyre argue that Hume
    himself allows for a kind of inference from “is” to “ought” in other
    places. (Cf. @arnhart1995new; @macintyre1959hume) I think Moore
    deserves more of the blame (or the credit).

[^12]: The Greek word ‘*telos*’ is commonly translated as “end,” but it
    is bursting with an array of possible meanings, including: “definite
    point,” “goal,” “purpose,” “cessation,” “order,” “prize,” “highest
    point,” “realization,” “decision,” and “services.” See
    @liddell1896intermediate. Strong fills out this already rich picture
    with a wider array of related meanings from the Koine Greek: “from a
    primary *tello* (to set out for a definite point or goal); properly,
    the point aimed at as a limit, i.e. (by implication) the conclusion
    of an act or state (termination (literally, figuratively or
    indefinitely), result (immediate, ultimate or prophetic), purpose);
    specially, an impost or levy (as paid); continual, custom,
    end(-ing), finally, uttermost.” See *Strong’s Exhaustive
    Concordance: New American Standard Bible.* Updated ed. La Habra:
    Lockman Foundation, 1995. Entry 5056.

[^13]: One might say that some things – God or people or platonic forms
    – are *good full stop*. I shall concede that God, say, would not
    have a complement like this. But is any creature good simpliciter?
    Even so, calling God *good full stop* is a way of indicating that he
    is good *for everyone and everything*. He is the unqualifiedly
    desirable, or rather, he is desirable *to anything capable of
    desiring*. The Psalmist says “let everything that has breath praise
    the Lord.” Presumably, objects without breath are relieved of the
    obligation, even if their authorship and grounding is in him.

[^14]: @thompson2008life, chapter 1.

[^15]: @blackman2015meta. Blackman also disputes the kind of biological
    foundation of ethics I am trying to defend here. Nevertheless, his
    article is a good introduction into the sort of “kindism” being
    discussed.

[^16]: While scientific realism is not uncontroversial per se, my
    intended audience are committed scientific realists or sympathetic
    to realism. McDowell, as a sort of idealist, will dispute even my
    modest scientific realism, as we shall see in chapter 6.

[^17]: @anscombe1958

[^18]: @carlson1977unified. Carlson’s essay is an early attempt to
    account for a variety of linguistic forms under one concept of
    reference to kinds

[^19]: Cf. @pelletier1995generic; @leslie2008generics;
    @bailey2015animalism for a discussion of a specific generic: “we are
    animals” in metaphysics and philosophical anthropology;
    @cimpian2010generic for an experiment in cognitive psychology that
    seeks to quantify the prevalence levels at which subjects tend to
    agree to generics: e.g., how many birds have to lay eggs before we
    agree to the assertion that “birds lay eggs”? @krifka2003bare;
    @cohen2001generic.

[^20]: A shark looking up may miss a penguin, because its white belly
    blends in with the sunlit surface waters; a shark looking down may
    miss a penguin, because it blends in with the pitch dark waters of
    the abyss.

[^21]: The proponent of a view of nature in which all material objects
    instantiate normative properties would reject the label ‘enchanted.’
    The term ‘enchantment’ presumes that an object has no intrinsic
    evaluative properties but receives them, like a spell, from the
    evaluator. The issue cannot be settled by presumption. Nevertheless,
    this issue is not my main focus.

[^22]: Barham, “Teleological Realism in Biology,” chapter 3. My
    discussion will closely follow this chapter; however, Barham’s
    discussion is far too rich to be condensed into the space available
    here.

[^23]: Cf. Perlman, “The Modern Philosophical Resurrection of
    Teleology,” section III; and Barham, “Teleological Realism in
    Biology,” chapter 3.

[^24]: @perlman2004teleology" 6. One might suppose that Perlman’s
    qualification “or at least in practice does not” leaves open space
    for the normative anti-realist. I welcome the critic who would try
    to show that biology *can* eliminate functions; what I have tried to
    suggest, and what Barham argues in great detail, is that the attempt
    has been made and has failed. A few failed attempts at reduction
    does not prove that reduction is impossible. But it does make the
    more plausible view, teleological realism, a better candidate for
    the default view.

[^25]: @barham 111.

[^26]: Thus Godfrey-Smith’s summary: Evolution by natural selection is
    change in a population due to: (i) variation in the characteristics
    of members of the population, (ii) which causes different rates of
    reproduction, and (iii) which is inherited. (@godfrey2007conditions,
    515). This is only one of Godfrey-Smith’s two descriptions: the more
    general description excludes particular real organisms in exchange
    for a useful degree of generality.

[^27]: “Although the most general principles in nature ought to be held
    merely positive, as they are discovered, and cannot with truth be
    referred to a cause, nevertheless the human understanding being
    unable to rest still seeks something prior in the order of nature.
    And then it is that in struggling toward that which is further off
    it falls back upon that which is nearer at hand, namely, on final
    causes, which have relation clearly to the nature of man rather than
    to the nature of the universe; and from this source have strangely
    defiled philosophy.” Cf. *New Organon*, Book I. XLVIII.

[^28]: @chorost2013thomas.

[^29]: Admittedly, it sounds rather odd to say that an ‘ought’ can be a
    brutely normative natural fact. In chapter 6, I shall dissipate the
    oddity by offering a thorough discussion of the concept of ‘nature.’

[^30]: @hursthouse1998virtue 217.

[^31]: As Michael Mautner explains, all living things (on earth at
    least) share common ancestors and even share genetic material:
    “…phylogenetic trees indicate that all terrestrial life can be
    traced to a common ancestor. Organisms as different from us as
    yeasts share half; mice, over 90%, chimpanzees, over 95%, and
    different human individuals share over 99% of our genome. These
    scientific insights give a deeper meaning to the unity of all Life.
    Our complex molecular patterns are common to all organic
    gene/protein life and distinguish us from any other phenomena of
    nature.” @mautner2009life.

[^32]: I shall return to this theme in chapter 5. Throughout, I use the
    term ‘practical rationality’ as a synonym for ‘practical reason.’
    Warren Quinn uses ‘practical reason’ to mean the faculty and
    ‘practical rationality’ to mean the excellence use of the faculty.
    Cf. @quinn1992rationality.

[^33]: Cf. @foot2001natural, chapter 4; McDowell, “Virtue and Reason”;
    @macintyre1988whose.

[^34]: *Politics*, 1.1253a. Aristotle and the translator use the term
    ‘man’ in the gender inclusive sense.

[^35]: The biological claims include the following: The earth, which is
    very old, has given rise to simple life forms which have become over
    slow and gradual changes given rise to myriad life forms, some of
    which are very complex. The driving mechanism of this process is
    natural selecting acting on the genetic mutations of a given
    population. All of life originated from one original place and
    species. A philosophical claim, often appended to the biological
    ones, is that the process of natural selection is *unguided by any
    causes but material-efficient mechanical ones.* But this claim is a
    philosophical belief, not a biological one. Polemicists will
    sometimes cite the popularity of the philosophical belief among
    biologists as proof that it is a “biological” claim. But we do not
    determine truth by vote. If belief in God was popular among
    biologists of a certain era, it does not follow that theological
    claims are strictly biological claims.

[^36]: This worry is developed in detail by Hursthouse (*On Virtue
    Ethics* Chapter 10) and Stephen Brown (*Moral Virtue and Nature*
    chapter 5) and Ward, “Against Natural Teleology and Its Application
    in Ethical Theory.” All three think that ethics is not ultimately
    scientific.

[^37]: For example, a non-naturalist or religious philosopher could
    concede that humans are *partly* natural but would argue that human
    beings are exceptional in some way – in virtue of being endowed by
    God with the *Imago Dei*, or enjoying unique cognitive faculties
    such as practical reasoning. For present purposes, I am bracketing
    this discussion.

[^38]: The “Voluntary Human Extinction Movement” (VHEMT) is an example
    of a group who find the reasons for reproduction *as a species* to
    be on balance outweighed by the reasons for ceasing to reproduce.
    Two comments: first, on first impression, VHEMT strikes most people
    as satire. It is a laughable movement. It is not necessarily
    mistaken, but it is certainly laughable. Secondly, VHEMT
    acknowledges the prima facie force of the need to reproduce. They
    argue that the need is outweighed. So in that they think
    species-wide reproduction is a default natural norm, we agree.

[^39]: I derive their views from a variety of sources. Foot’s concept of
    virtue and practical reason I derive not only from *Natural
    Goodness* but from her “Virtues and Vices” essay. For MacIntyre, I
    draw from *After Virtue*, where he builds his three stage account of
    virtue (relating to practice, then life, then tradition) from a
    careful study of the history of the concept within the broader
    western tradition. But I also draw from *Whose Justice? Which
    Rationality?*, *Three Rival Versions of Moral Inquiry*, and
    *Dependent Rational Animals*. McDowell’s writings on virtue and
    reason span several essays and books, such as *Mind, Value and
    Reality*. I especially draw from “Virtue and Reason” and “Values as
    Secondary Qualities.”

[^40]: Her exact words are that virtue is excellence of “the rational
    will.” After expanding the concept of ‘will’ beyond its typical
    meaning to include intentions, it is clear her ‘rational will’ is
    identical to my ‘practical rationality.’ I want to avoid the word
    will because it might be a narrowly western way of viewing the
    capacity for practical reasoning. David Bradshaw distinguishes the
    cluster of concepts such as heart, mind, and will, and shows that
    Aristotle and others did not have a concept of a distinct,
    sub-rational faculty for choosing. Cf. @Bradshaw2009mind.

[^41]: Presumably, the point of specifying that virtues are *human*
    qualities here is to contrast human excellence with analogous formal
    or functional biological features that enable non-human animals to
    survive and thrive (e.g., the flexible flagellum of a bacterium, the
    swiftness of a deer. For MacIntyre’s initial formulation here, such
    biological features are excluded from the class of virtues by
    definition; his later *Dependent Rational Animals* retracts the
    assumed divide between human and non-human animals.

[^42]: For example, Smith: All Scotsmen love haggis. Jones: But McDougal
    over there is a Scotsman, and he hates haggis. Smith: That just goes
    to show McDougal is no *true* Scotsman. Cf. @flew1975thinking

[^43]: Many polyglots are known to have mastered upwards of 20
    languages. Some, such as Sir John Bowring, knew as many as a
    hundred.

[^44]: As we shall see in McDowell’s discussion of virtue-as-knowledge
    in chapter 5, it might be that when we admire a person’s courage or
    moderation, we are often admiring the wisdom *in* the courage and
    the wisdom *in* the moderation.

[^45]: In the first line of Plato’s *Meno*, Meno asks Socrates a
    question “whether virtue is acquired by teaching or by practice; or
    if neither by teaching nor practice, then whether it comes to man by
    nature, or in what other way?” @plato, *Meno* 70a. While Plato gives
    hints as to his answer, Socrates himself punts on the question of
    how virtue is acquired and directs Meno to what virtue is. Moral
    philosophers have continued to try to answer this question for the
    last 2,400 years. That said, my goal here is not to address *how*
    virtue is acquired. My only goal here is to argue that a trait must
    be *acquirable* to be a virtue.

[^46]: *Hamlet* III.1

[^47]: Julia Annas’s argument that virtues are skills of a particular
    type takes advantage of the intuitive similarity between virtue and
    skill. Cf. @annas2011intelligent.

[^48]: MacIntyre, “Social Science Methodology as the Ideology of
    Bureaucratic Authority,” in *Through the Looking Glass: Epistemology
    and the Conduct of Inquiry*, Maria J. Falco, ed. (University Press
    of America, 1979) 42-58. Reprinted in Kelvin Knight, ed. *The
    MacIntyre Reader,* 55

[^49]: To illustrate the temptation goods of effectiveness might pose,
    we need only think about political activity. Some (I suppose) become
    politicians *in order to bring about* the survival, security, and
    prosperity of the *polis*; others engage in order merely to satisfy
    their own ambition or achieve fame. Often we see American
    politicians running for office only one apparent aim: book sales.

[^50]: Stanley Hauerwas, “The Virtues of Alasdair MacIntyre,” *First
    Things* (2007). Web. The quotation is from MacIntyre, *After Virtue*
    209.

[^51]: The term comes, I believe, from Ricoeur, who said: “Three
    masters, seemingly mutually exclusive, dominate the school of
    suspicion: Marx, Nietzsche, and Freud.” (@ricoeur1970freud 32)

[^52]: His 1977 essay on epistemological crises was his own version of
    Kuhn’s *Structure of Scientific Revolutions* – we might call this
    essay MacIntyre’s “Structure of Ethical Revolutions.” Cf.
    @macintyre1977epistemological

[^53]: Compare with @cuneo2014speech.

[^54]: “It might be thought that ordinary conceptions of rationality are
    Platonistic or intuitionistic. On the Platonistic picture, among the
    facts of the world are facts of what is rational and what is not. A
    person of normal mental powers can discern these facts. Judgments of
    rationality are thus straightforward apprehensions of fact, not
    through sense perception but through a mental faculty analogous to
    sense perception. When a person claims authority to pronounce on
    what is rational, he must base his claim on this power of
    apprehension.” See @gibbard1992wise 154.

[^55]: He says: “Reason is the discovery of truth and falsehood.”
    (*Treatise of Human Nature*, Part I.1.)

[^56]: We all exhibit various dispositions to act in certain ways, to
    rank and organize our various motivations, to pursue certain things,
    or to make certain decisions rather than others. Such dispositions
    are clearly practical. They have the right kind of action-guiding
    force to explain why we act the way we do. On the other hand, there
    are dispositions. The term ‘disposition’ gets used in various ways:
    one can be disposed (say) to repay one’s debts (a moral commitment),
    or disposed to shout when angry (a temperament), or disposed to
    travel abroad every summer (an interest). But is a “disposition” a
    form of knowledge?

[^57]: The relation between virtue and happiness or self-regard is an
    expansive one: For fuller treatments, one might begin with:
    @macintyre1967egoism. @slote1995agent. @annas2009egoism.
    @huang2010self. @bloomfield2012eudaimonia.

[^58]: @pincoffs1971quandary 552. MacIntyre offers a criticism along
    similar lines to Pincoffs in his “Does Applied Ethics Rest on a
    Mistake?”

[^59]: @foot2002virtues chapter 13, “Are Moral Reasons Overriding?”; Cf.
    also @mcdowell1978moral

[^60]: Foot says: “It is my opinion that the *Summa Theologica* is one
    of the best sources we have for moral philosophy, and moreover that
    St. Thomas’s ethical writings are as useful to the atheist as to the
    Catholic or other Christian believer.” (*Virtues and Vices*, 2.)

[^61]: For a discussion of this distinction, see: @hooker2004procedural.

[^62]: Non-cognitivism is motivated by metaphysical naturalism, which
    objects to normative realism about practical reasons. I shall
    address that objection in chapter 6.

[^63]: @andreou2006getting; @millgram2005reasonably;
    @woodcock2006philippa.

[^64]: Virginia Morell (2014, March 28). “Why Do Animals Sometimes Kill
    Their Babies?” *National Geographic* (March 28, 2014). Accessed
    online.
    http://news.nationalgeographic.com/news/2014/03/140328-sloth-bear-zoo-infanticide-chimps-bonobos-animals/

[^65]: Wittgenstein, *Philosophical Investigations.* Section 124.

[^66]: *Bildung* (German): formation, education; from *bild*: form,
    image.

[^67]: Cf. @mcdowell1996mind. Chapter 6.

[^68]: @fink 219, quoting *Mind, Value, and Reality* 112-31, especially
    section 5. Roy Wood Sellars provides a pure specimen of such
    ideological question-begging: “I mean that naturalism takes nature
    in a definite way as identical with reality, as self-sufficient and
    as the whole of reality. And by nature is meant the
    space-time-causal system which is studied by science and in which
    our lives are passed.” (@sellars1927naturalism 217) Note that the
    first sentence explicitly endorses an unrestricted conception of
    nature while the next sentence secretly slides the ball into the
    other cup, overtly stipulating that the “space-time-causal system
    which is studied by science and in which our lives are passed” is
    “identical with reality.” Whether that stipulation is true is the
    very question at hand. No one disputes that unrestricted nature is
    all there is; but some do dispute the implicit assumption that the
    space-time-causal-system is all there is to nature.

[^69]: McDowell would vehemently deny this charge. (Cf.
    @mcdowell1996mind, Lecture VI.) My point is not that he admits to
    embracing reason/body dualism but that his explicit view entails it.

[^70]: See Frey, “The Will and the Good,” 44, footnote 55.

[^71]: I take my view to be similar to those defended, especially in
    “Miracle of Monism” and “The Inseparability of Science and Values”
    by John Dupre. *Processes of Life: Essays in the Philosophy of
    Biology.* (Oxford University Press; 2012).

[^72]: Paraphrasing Frederich Nietzsche, *The Gay Science*, section 344.

[^73]: Cf. “For a well schooled man searches for that degree of
    precision in each kind of study which the nature of the subject at
    hand admits: is obviously just as foolish to accept arguments of
    probability from a mathematician has to demand strict demonstrations
    from an orator.” Aristotle, *Nicomachean Ethics*, Book I.3

\end{document}