# latex-report-template

From overleaf
https://www.overleaf.com/latex/templates/shortpaper-template/dcwrzxdkwfcy

---

                            General comments about Overleaf/LaTeX

---

\ is the god of commands in LaTeX.

LaTeX is a coded text editor. In general I have already set up the document outline so not much backbone editting is needed.

PLEASE don't edit \textbf{packages.tex} or main.tex without knowing what you are doing first. Some packages need to be in a certain place in the compiling order, conflict with other packages or give other problems. The main.tex file basically grabs together all the different sections of text that are in the 'sections' folder and creates the final document.

I try to keep my LaTeX code understandable by using comments and sectioning formatting code by using comment blocks as above, it might be a good practice to do the same if you ever want to programme the formatting as well.

I will now explain a few basic commands:

\\ - Enter; Two \\ \\ creates a white rule (\\ followed by an empty coding line essentially does this too)

$<equation>$ - stuff between dollar signs will be in mathmode, meaning that you can use math commands. The return will be intext.
Equations for math mode:
\beta, \alpha, etc.
\frac{}{}
\pm (plus minus sign)
\sqrt{}
\_ subscript
^ superscript (also used for powers)

\begin{}; begins a command environment, the most used for beginners are:
\begin{figure} - by using tab at the suggestion you auto fill a basic figure environment
\begin{table} - this trick works for many commands
\begin{equation} - will return a number inline equation
\begin{equation\*} - will return a unnumbered inline equation

\cite{} ; adds a cite in the text, first add reference in bibtex format in references.bib, then you can use it in the text or in captions

\autoref{} ; adds a reference to something that is labelled, this can be pictures/tables/sections/anything. Autoref also includes what it is; so if the label is attached to a figure the \autoref command will return something like 'Figure xx' in the text
\ref{} ; does the same as autoref but doesn't include what it is; so it will only give 'xx' in the above case.

Basic figure environment:
\begin{figure}[<float specifier>]
\centering
\includegraphics[size]{<figurepath>}
\caption{Caption}
\label{fig:my_label}
\end{figure}]

Sections: to add sections you can use the following command:
\section{<title here>} - will create a numbered section
\section\*{<title here>} - will create an unnumbered section
\subsection{} - also works with the asterisk to make unnumbered
\subsubsection{} etc.

LaTeX uses floating boxes to put stuff in. In the above case you create the box with the \begin{figure} enviroment. The \centering command centers the graphics that you include in the middle of the box. With \includegraphics[]{} you first specify the size, a much used parameter is [width=\textwidth], making the picture as wide as the textwidth. Secondly you define the figurepatch, overleaf will prefill this for you, if you uploaded the picture into the document (use the images folder), it will become something like "Images/<figurename>.jpg". The \caption command does what you think it does. The \label{} should be placed after a caption at all times, and allows you to \ref{} or \autoref{} the figure in the text.
