# NCL language definition for use with the LaTeX "listings" package

If you use `minted`, I can't help you (yet).

To use it, just download the [`.tex`](https://github.com/thymaro/ncl-tex-listings/blob/master/ncl-tex-listings.tex) (right-click and choose "save destination file" or similar), put it next to your main `.tex` document in the same directory and write the following line in your preamble:

```tex
\input{ncl-tex-listings}
```    
If you found this page, I figure you already know this, but in case you don't: you also need to load the `listings` package and you also might want to add settings to your listings. For instance, I use the following in combination with NCL:

```tex
\usepackage{listings}

\lstset{ <-- add a percent sign here, but I can't do it, it breaks github pages compilation.
        language=ncl,
	escapeinside={(*}{*)},
	% FRAME
	frame=single,
	backgroundcolor=\color{gray!15},
	% SURROUNDINGS
	numberfirstline=true,
	firstnumber=1,
	numbers=left,
	numbersep=5pt,
	numberstyle=\tiny,
	stepnumber=5,
	captionpos=b,
	% CODE EMBELLISHMENTS
	breakatwhitespace=false,
	breaklines=true,
	keepspaces=false,
	showstringspaces=false,
	showtabs=true,
	tab=\rightarrowfill,
	tabsize=3,
	% FONT STYLES
	basicstyle=\small\ttfamily,
	commentstyle=\color{green!70!black}\itshape,
	keywordstyle=\color{teal!70!black}\bfseries,
	stringstyle=\color{red!65!black},
	identifierstyle=\color{orange!30!black},
}
```


If you are using _TeXstudio_ (like I am), hit and hold `Ctrl`, then click on `ncl-tex-listings` (which has now magically morphed into a clickable link) to check, if the file is found. If it isn't, I can think of three error sources
+ you didn't download the file
+ you downloaded the file to another directory than the one you should have. Please check your 'downloads' directory.
+ you changed the name of the file. Why?
  + okay, I don't really wanna know. Anyways, in this case, change `\input{ncl-tex-listings}` to `\input{whatever-shabby-name-you-named-your-file}` and it should work.

Learn how to access the file anyway. Look it up on [tex.se](tex.stackexchange.com) or whencever you get your T<sub>E</sub>X-knowledge.

Ok, nuff kiddin'. I know nobody will ever read this. I mean, who on earth uses TeX **and** NCL in one sitting?! You nerds!

Nevertheless, if you see a way to improve on this file, please feel free to fork it and add a pull request.
