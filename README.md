# github-page-test

content 

## subsection

list
* item
* item
* item

[link](github.com)

*emphasis*

{% raw %}
```tex
% beamerbasesection.sty, line 256:
\def\beamer@subsection[#1]#2{%
  \beamer@savemode%
  \mode<all>%
  \ifbeamer@inlecture%
    \refstepcounter{subsection}%
    \ifblank{#2}{\long\def\subsecname{#1}\long\def\lastsubsection{#1}}
    {%
      \long\def\subsecname{#2}%
      \long\def\lastsubsection{#1}%
      \addtocontents{toc}{\protect\beamer@subsectionintoc{\the\c@section}{\the\c@subsection}{#2}{\the\c@page}{\the\c@part}{\the\beamer@tocsectionnumber}}%
    }%
    \beamer@tempcount=\c@page\advance\beamer@tempcount by -1%
    \addtocontents{nav}{\protect\headcommand{\protect\beamer@subsectionpages{\the\beamer@subsectionstartpage}{\the\beamer@tempcount}}}
    \ifblank{#1}{}{%
      \addtocontents{nav}{\protect\headcommand{\protect\beamer@subsectionentry{\the\c@part}{\the\c@section}{\the\c@subsection}{\the\c@page}{\lastsubsection}}}
    }%
    \beamer@subsectionstartpage=\c@page%
    \edef\subsectionlink{{Navigation\the\c@page}{\noexpand\subsecname}}%
    \def\insertsubsection{\expandafter\hyperlink\subsectionlink}%
    \def\insertsubsubsection{}%
    % Deal with a faulty patch in metropolis theme
    \def\insertsubsectionhead{\hyperlink{Navigation\the\c@page}{#1}}%
    \edef\insertsubsectionhead{\noexpand\hyperlink{Navigation\the\c@page}{\unexpanded{#1}}}%
    \def\insertsubsubsectionhead{}%
    \Hy@writebookmark{\the\c@subsection}{\subsecname}{Outline\the\c@part.\the\c@section.\the\c@subsection.\the\c@page}{3}{toc}%
    \hyper@anchorstart{Outline\the\c@part.\the\c@section.\the\c@subsection.\the\c@page}\hyper@anchorend%
    \ifblank{#2}{\beamer@atbeginsubsections}{\beamer@atbeginsubsection}%
  \fi%
  \beamer@resumemode}
```
{% endraw %}
