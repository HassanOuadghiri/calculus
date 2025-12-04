\documentclass{article}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{geometry}
\geometry{margin=1in}

\title{Calculus Explained Simply: A Guide for Beginners}
\author{}
\date{}

\begin{document}
\maketitle

\section{Part 1: Derivatives (The Speedometer)}

\subsection{What is a Derivative?}
Imagine you are driving a car. 
\begin{itemize}
    \item Your \textbf{position} is where you are on the map.
    \item The \textbf{derivative} is your \textbf{speedometer}. It tells you exactly how fast you are changing your position at this exact moment.
\end{itemize}

In math, the derivative tells us the \textbf{slope} of a curve at a specific point. Is the graph going up steep? Is it flat? Is it going down? The derivative gives you a number for that steepness.

\textbf{Notation:} If the function is $f(x)$, the derivative is written as $f'(x)$ (read "f prime of x") or $\frac{dy}{dx}$.

\subsection{The Power Rule (The "Hop and Drop" Trick)}
This is the easiest way to find a derivative for normal numbers.

\textbf{The Rule:} If you have $x^n$, you bring the $n$ down to the front, and subtract 1 from the power.
$$\frac{d}{dx}(x^n) = n \cdot x^{n-1}$$

\textbf{Example:} Let's find the derivative of $x^3$.
\begin{enumerate}
    \item Take the 3 and hop it to the front: $3x^3$
    \item Drop the power by 1 ($3-1=2$): $3x^2$
    \item \textbf{Answer:} $3x^2$
\end{enumerate}

\subsubsection*{ \textbf{NOTES \& TIPS:}}
\begin{itemize}
    \item \textbf{The Invisible 1:} If you just have $x$, the derivative is $1$. (Because $x$ is really $x^1$. Bring 1 down, get $x^0$, which is 1).
    \item \textbf{The Constant Killer:} The derivative of any plain number (like 5, 100, or $\pi$) is always \textbf{0}. Why? Because a number doesn't change! Its slope is flat.
    \item \textbf{Multipliers Stay:} If you have $4x^3$, the 4 just sits there waiting. You do the power rule on $x^3$ (which is $3x^2$) and multiply it by the 4. Result: $12x^2$.
\end{itemize}

\subsection{Common Derivatives Cheat Sheet}
Memorize these! They appear everywhere.
\begin{itemize}
    \item $\sin(x) \rightarrow \cos(x)$
    \item $\cos(x) \rightarrow -\sin(x)$ \quad (\textit{Watch out for the negative sign!})
    \item $e^x \rightarrow e^x$ \quad (\textit{The easiest one! It never changes.})
    \item $\ln(x) \rightarrow \frac{1}{x}$
\end{itemize}

\newpage

\section{Part 2: Integrals (The Area / The Reverse)}

\subsection{What is an Integral?}
Integration is just \textbf{Derivatives in Reverse}. 
\begin{itemize}
    \item If a derivative takes a whole chicken and chops it into nuggets...
    \item An integral takes the nuggets and glues them back into a chicken.
\end{itemize}
It is also used to find the \textbf{Area} underneath a curvy line.

\textbf{Notation:} The symbol is a tall, skinny "S": $\int$

\subsection{The Power Rule for Integrals}
Since this is the reverse of derivatives, we do the opposite steps.
\begin{enumerate}
    \item Add 1 to the power.
    \item Divide by that new number.
\end{enumerate}

$$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C$$

\textbf{Example:} Integrate $x^2$.
\begin{enumerate}
    \item Add 1 to the power ($2+1=3$): $x^3$
    \item Divide by that new number (3): $\frac{x^3}{3}$
    \item \textbf{Answer:} $\frac{x^3}{3} + C$
\end{enumerate}

\subsubsection*{ \textbf{CRITICAL NOTES:}}
\begin{itemize}
    \item \textbf{Don't Forget + C:} When you integrate without limits (numbers on the S), you \textbf{MUST} write $+ C$ at the end. 
    \item \textbf{Why + C?} Because the derivative of a constant is 0. If we go backwards, we don't know if the original function had a $+5$ or a $+100$ at the end. So we just write $+C$ to mean "plus some number."
    \item \textbf{The Exception:} You cannot use the power rule for $x^{-1}$ (which is $\frac{1}{x}$). If you add 1 to -1, you get 0, and you can't divide by 0! The integral of $\frac{1}{x}$ is $\ln|x|$.
\end{itemize}

\newpage

\section{Part 3: Limits (The "Approaching" Game)}

\subsection{What is a Limit?}
A limit asks: "Where is the function \textit{trying} to go?"
It doesn't matter if it actually gets there. It just matters where the path leads.

$$\lim_{x \to 2} f(x)$$
This reads: "The limit of f(x) as x gets closer and closer to 2."

\subsection{How to Solve Limits}
\begin{enumerate}
    \item \textbf{Method 1: Just Plug It In (Direct Substitution)}
    \textit{Try this first!} If you want the limit as $x \to 5$, just put 5 into the equation.
    $$ \lim_{x \to 5} (x + 2) = 5 + 2 = 7 $$
    
    \item \textbf{Method 2: Factor and Cancel (The "Hole" Fixer)}
    If you plug it in and get $\frac{0}{0}$, that's bad. It means there is a hole in the graph.
    \begin{itemize}
        \item Factor the top and bottom.
        \item Cross out the matching parts.
        \item Plug the number in again.
    \end{itemize}
    
    \item \textbf{Method 3: L'Hôpital's Rule (The Emergency Button)}
    If you get $\frac{0}{0}$ or $\frac{\infty}{\infty}$, you can take the derivative of the top AND the derivative of the bottom separately, then try again.
\end{enumerate}

\section{Part 4: Continuity (The Pencil Test)}

\subsection{What is Continuity?}
A function is continuous if the line never breaks.

\textbf{The Pencil Test:} Can you draw the whole graph without lifting your pencil off the paper? If yes, it's continuous!

\subsection{The 3 Rules of Continuity}
For a function to be continuous at a point $c$:
\begin{enumerate}
    \item \textbf{The point exists:} There is actually a dot there ($f(c)$ is defined).
    \item \textbf{The limit exists:} The road leads to the same place from the left and the right.
    \item \textbf{They match:} The road leads exactly to where the dot is.
\end{enumerate}

\subsubsection*{ \textbf{Types of Breaks (Discontinuities):}}
\begin{itemize}
    \item \textbf{Hole (Removable):} The road is perfect, but someone stole the manhole cover. (Limit exists, but the point is missing).
    \item \textbf{Jump:} The road suddenly teleports up or down. (Left side $\neq$ Right side).
    \item \textbf{Asymptote (Infinite):} The road goes on forever in one direction (up or down). The function is not defined there.
\end{itemize}

\end{document}# University Calculus Reference Guide

## 1. Sequences and Limits

### Sequences
A sequence is an ordered list of numbers $\{a_n\}_{n=1}^{\infty}$.

**Definition:**
A sequence $\{a_n\}$ converges to a limit $L$ if for every $\epsilon > 0$, there exists an integer $N$ such that for all $n > N$, $|a_n - L| < \epsilon$.
Notation: $\lim_{n \to \infty} a_n = L$.

### Limits of Functions
**Definition:**
Let $f(x)$ be defined on an open interval containing $c$ (except possibly at $c$). We say $\lim_{x \to c} f(x) = L$ if for every $\epsilon > 0$, there exists a $\delta > 0$ such that if $0 < |x - c| < \delta$, then $|f(x) - L| < \epsilon$.

#### Limit Laws
If $\lim_{x \to c} f(x) = L$ and $\lim_{x \to c} g(x) = M$:
*   **Sum:** $\lim_{x \to c} [f(x) + g(x)] = L + M$
*   **Product:** $\lim_{x \to c} [f(x)g(x)] = LM$
*   **Quotient:** $\lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$ (provided $M \neq 0$)

#### The Squeeze Theorem
If $g(x) \leq f(x) \leq h(x)$ near $c$ and $\lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$, then $\lim_{x \to c} f(x) = L$.

#### Special Trigonometric Limits
$$ \lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{and} \quad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0 $$

### Continuity
A function $f$ is continuous at $c$ if:
1.  $f(c)$ is defined.
2.  $\lim_{x \to c} f(x)$ exists.
3.  $\lim_{x \to c} f(x) = f(c)$.

**Theorem (Intermediate Value Theorem):**
If $f$ is continuous on $[a,b]$ and $k$ is any number between $f(a)$ and $f(b)$, there exists at least one $c \in (a,b)$ such that $f(c) = k$.

## 2. Differentiation

### Definition of the Derivative
The derivative of $f$ at $x$ is defined as:
$$ f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} $$

### Differentiation Rules
Let $u$ and $v$ be differentiable functions of $x$.
*   **Power Rule:** $\frac{d}{dx}(x^n) = nx^{n-1}$
*   **Product Rule:** $\frac{d}{dx}(uv) = u'v + uv'$
*   **Quotient Rule:** $\frac{d}{dx}\left(\frac{u}{v}\right) = \frac{u'v - uv'}{v^2}$
*   **Chain Rule:** $\frac{d}{dx}[f(g(x))] = f'(g(x))g'(x)$

### Common Derivatives
$$
\begin{aligned}
    \frac{d}{dx}(\sin x) &= \cos x & \frac{d}{dx}(\cos x) &= -\sin x \\
    \frac{d}{dx}(\tan x) &= \sec^2 x & \frac{d}{dx}(\cot x) &= -\csc^2 x \\
    \frac{d}{dx}(\sec x) &= \sec x \tan x & \frac{d}{dx}(\csc x) &= -\csc x \cot x \\
    \frac{d}{dx}(e^x) &= e^x & \frac{d}{dx}(\ln x) &= \frac{1}{x} \\
    \frac{d}{dx}(\sin^{-1} x) &= \frac{1}{\sqrt{1-x^2}} & \frac{d}{dx}(\tan^{-1} x) &= \frac{1}{1+x^2}
\end{aligned}
$$

### Theorems
**Theorem (Mean Value Theorem):**
If $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, there exists $c \in (a,b)$ such that:
$$ f'(c) = \frac{f(b) - f(a)}{b - a} $$

**Theorem (L'Hôpital's Rule):**
If $\lim_{x \to c} \frac{f(x)}{g(x)}$ yields $\frac{0}{0}$ or $\frac{\infty}{\infty}$, then:
$$ \lim_{x \to c} \frac{f(x)}{g(x)} = \lim_{x \to c} \frac{f'(x)}{g'(x)} $$

## 3. Integration

### Definite and Indefinite Integrals
*   **Indefinite:** $\int f(x) \, dx = F(x) + C$, where $F'(x) = f(x)$.
*   **Definite:** $\int_a^b f(x) \, dx$ represents the net signed area under the curve.

### Fundamental Theorem of Calculus
**Part 1:** If $g(x) = \int_a^x f(t) \, dt$, then $g'(x) = f(x)$.
**Part 2:** If $F$ is any antiderivative of $f$, then $\int_a^b f(x) \, dx = F(b) - F(a)$.

### Integration Techniques
#### u-Substitution (Reverse Chain Rule)
Let $u = g(x)$, then $du = g'(x)dx$.
$$ \int f(g(x))g'(x) \, dx = \int f(u) \, du $$

#### Integration by Parts (Reverse Product Rule)
$$ \int u \, dv = uv - \int v \, du $$

### Common Integrals
$$
\begin{aligned}
    \int x^n \, dx &= \frac{x^{n+1}}{n+1} + C \quad (n \neq -1) \\
    \int \frac{1}{x} \, dx &= \ln|x| + C \\
    \int e^x \, dx &= e^x + C \\
    \int \frac{1}{1+x^2} \, dx &= \tan^{-1} x + C \\
    \int \frac{1}{\sqrt{1-x^2}} \, dx &= \sin^{-1} x + C \\
    \int e^{ax} \, dx &= \frac{1}{a}e^{ax} + C \\
    \int \cos(ax) \, dx &= \frac{1}{a}\sin(ax) + C \\
    \int \sin(ax) \, dx &= -\frac{1}{a}\cos(ax) + C
\end{aligned}
$$

\newpage

# University Calculus Reference Guide

## 1. Sequences and Limits

### Sequences
A sequence is an ordered list of numbers $\{a_n\}_{n=1}^{\infty}$.

**Definition:**
A sequence $\{a_n\}$ converges to a limit $L$ if for every $\epsilon > 0$, there exists an integer $N$ such that for all $n > N$, $|a_n - L| < \epsilon$.
Notation: $\lim_{n \to \infty} a_n = L$.

### Limits of Functions
**Definition:**
Let $f(x)$ be defined on an open interval containing $c$ (except possibly at $c$). We say $\lim_{x \to c} f(x) = L$ if for every $\epsilon > 0$, there exists a $\delta > 0$ such that if $0 < |x - c| < \delta$, then $|f(x) - L| < \epsilon$.

#### Limit Laws
If $\lim_{x \to c} f(x) = L$ and $\lim_{x \to c} g(x) = M$:
*   **Sum:** $\lim_{x \to c} [f(x) + g(x)] = L + M$
*   **Product:** $\lim_{x \to c} [f(x)g(x)] = LM$
*   **Quotient:** $\lim_{x \to c} \frac{f(x)}{g(x)} = \frac{L}{M}$ (provided $M \neq 0$)

#### The Squeeze Theorem
If $g(x) \leq f(x) \leq h(x)$ near $c$ and $\lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$, then $\lim_{x \to c} f(x) = L$.

#### Special Trigonometric Limits
$$ \lim_{x \to 0} \frac{\sin x}{x} = 1 \quad \text{and} \quad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0 $$

### Continuity
A function $f$ is continuous at $c$ if:
1.  $f(c)$ is defined.
2.  $\lim_{x \to c} f(x)$ exists.
3.  $\lim_{x \to c} f(x) = f(c)$.

**Theorem (Intermediate Value Theorem):**
If $f$ is continuous on $[a,b]$ and $k$ is any number between $f(a)$ and $f(b)$, there exists at least one $c \in (a,b)$ such that $f(c) = k$.

## 2. Differentiation

### Definition of the Derivative
The derivative of $f$ at $x$ is defined as:
$$ f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} $$

### Differentiation Rules
Let $u$ and $v$ be differentiable functions of $x$.
*   **Power Rule:** $\frac{d}{dx}(x^n) = nx^{n-1}$
*   **Product Rule:** $\frac{d}{dx}(uv) = u'v + uv'$
*   **Quotient Rule:** $\frac{d}{dx}\left(\frac{u}{v}\right) = \frac{u'v - uv'}{v^2}$
*   **Chain Rule:** $\frac{d}{dx}[f(g(x))] = f'(g(x))g'(x)$

### Common Derivatives
$$
\begin{aligned}
    \frac{d}{dx}(\sin x) &= \cos x & \frac{d}{dx}(\cos x) &= -\sin x \\
    \frac{d}{dx}(\tan x) &= \sec^2 x & \frac{d}{dx}(\cot x) &= -\csc^2 x \\
    \frac{d}{dx}(\sec x) &= \sec x \tan x & \frac{d}{dx}(\csc x) &= -\csc x \cot x \\
    \frac{d}{dx}(e^x) &= e^x & \frac{d}{dx}(\ln x) &= \frac{1}{x} \\
    \frac{d}{dx}(\sin^{-1} x) &= \frac{1}{\sqrt{1-x^2}} & \frac{d}{dx}(\tan^{-1} x) &= \frac{1}{1+x^2}
\end{aligned}
$$

### Theorems
**Theorem (Mean Value Theorem):**
If $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, there exists $c \in (a,b)$ such that:
$$ f'(c) = \frac{f(b) - f(a)}{b - a} $$

**Theorem (L'Hôpital's Rule):**
If $\lim_{x \to c} \frac{f(x)}{g(x)}$ yields $\frac{0}{0}$ or $\frac{\infty}{\infty}$, then:
$$ \lim_{x \to c} \frac{f(x)}{g(x)} = \lim_{x \to c} \frac{f'(x)}{g'(x)} $$

## 3. Integration

### Definite and Indefinite Integrals
*   **Indefinite:** $\int f(x) \, dx = F(x) + C$, where $F'(x) = f(x)$.
*   **Definite:** $\int_a^b f(x) \, dx$ represents the net signed area under the curve.

### Fundamental Theorem of Calculus
**Part 1:** If $g(x) = \int_a^x f(t) \, dt$, then $g'(x) = f(x)$.
**Part 2:** If $F$ is any antiderivative of $f$, then $\int_a^b f(x) \, dx = F(b) - F(a)$.

### Integration Techniques
#### u-Substitution (Reverse Chain Rule)
Let $u = g(x)$, then $du = g'(x)dx$.
$$ \int f(g(x))g'(x) \, dx = \int f(u) \, du $$

#### Integration by Parts (Reverse Product Rule)
$$ \int u \, dv = uv - \int v \, du $$

### Common Integrals
$$
\begin{aligned}
    \int x^n \, dx &= \frac{x^{n+1}}{n+1} + C \quad (n \neq -1) \\
    \int \frac{1}{x} \, dx &= \ln|x| + C \\
    \int e^x \, dx &= e^x + C \\
    \int \frac{1}{1+x^2} \, dx &= \tan^{-1} x + C \\
    \int \frac{1}{\sqrt{1-x^2}} \, dx &= \sin^{-1} x + C \\
    \int e^{ax} \, dx &= \frac{1}{a}e^{ax} + C \\
    \int \cos(ax) \, dx &= \frac{1}{a}\sin(ax) + C \\
    \int \sin(ax) \, dx &= -\frac{1}{a}\cos(ax) + C
\end{aligned}
$$