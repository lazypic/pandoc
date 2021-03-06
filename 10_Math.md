
# Math
이 장에 관심이 있다면 논문, 학술자료, 공학, 교사에 관련된 직업일 확률이 높습니다.
글 또는 그림과 다르게 수학 기호와 수식은 그래프의 표현은 책을 집필할 때 어려움이 됩니다. 이 상황에서 Latex를 사용하면 유용합니다.
이 책은 LaTex, WebTex, MathML을 소개합니다. LaTex를 심도있게 다루고 나머지 솔루션은 소개정도만 다룹니다.
그럼 문서를 생성할 때 어떻게 수학의 기호나 그래프를 그리는지 알아보겠습니다.

## LaTex
LaTex는 오픈소스 조판시스템(Typesetting System)입니다.
조판작업이란 최종 결과물이 출력이 되기전에 출력될 결과물에 맞게 도형,수식,글을 배치하는 작업입니다.
LaTex를 이용해서 모든 형태를 그리고 배치할 수 있지만 대부분 수식, 그래프 작업이 필요할 때 일반적으로 많이 사용합니다.
또한 물리학자들을 위한 학술 커뮤니케이션 언어로 많이 사용됩니다. 어렵고 이상해 보이지만 35년이상 사용되면서 필요한 표기를 잘 처리할 수 있었습니다.
수식을 표현하는 솔루션은 LaTex, WebTex, MathML .. 등등 굉장히 많습니다.
수식을 모든 문서에 표기하기 위해서는 비효율적이지만 LaTex문법을 이용해서 이미지로 렌더링 후 문서에 첨부하는 형태를 많이 사용합니다.
불편하지만 다른 문서포멧으로 컨버팅 되더라도 문제없이 표시되기 때문입니다.
만약 공유와 협업이 필요한 상황에서는 [ShareLatex](https://www.sharelatex.com)를 사용하면 인터넷에서 친구들과 LaTex문서를 작성할 수 있습니다.

## LaTex 설치
macOS는 용량이 크지만 macTex를 설치하시면 관련된 솔루션을 한번에 해결할 수 있습니다.
MacTex 설치후 LaTexIt을 이용하면 미리결과를 보면서 LaTex문법을 타이핑할 수 있습니다.
또한 추후 재사용할 수 있도록 tex파일로 저장할 수 있습니다.

- 다운로드사이트 : http://www.tug.org/mactex/mactex-download.html

## LaTex문법
저는 수학에 사용하는 기호들도 한국어나 영어처럼 또다른 언어라고 생각합니다.
수학에서 사용하는 언어는 많은 뜻을 하나의 기호로 변경해서 사용하기 때문에 무척이나 함축적입니다.
처음에 보면 분명 외계어처럼 보이지만, 저는 다른 언어들처럼 자신이 필요한 만큼 배워서 사용하면 된다고 생각합니다.

이 챕터에서는 컴퓨터로 수학기호를 표현할 수 있는 LaTex의 수식표현 문법을 배워보겠습니다.
이 책은 Pandoc책이지만 Pandoc 만큼이나 LaTex를 조금 자세히 다루어 보는 책 입니다.
수학기호를 책에 넣기위해서 노력하다 보면 LaTex를 잘 다루고 있는 자료를 찾기위해서 매번 인터넷을 해메이기 때문입니다.
LaTex의 많은 문법들은 \\문자로 시작합니다.

### 4칙연산

덧셈에 대한 표현입니다. 우리가 사용하는 표현과 크게 다르지 않습니다.

$1 + 1 = 2$

```
1 + 1 = 2
```

뺄셈의 표현

$2 - 1 = 1$

```
2 - 1 = 1
```

곱셈의 표현

$2 \times 2 = 4$

```
2 \times 2 = 4
```

나눗셈의 표현

$4 \div 2 = 2$

```
4 \div 2 = 2
```

### 분수 / fraction
분수 영어로는 fraction. LaTex에서는 약자로 frac이라는 문법을 사용합니다.

$\frac{1}{2}$

```
\frac{1}{2}
```

### 요리에 자주 사용하는 분수
우리가 사용하는 기호중에 간장 1큰술반 같은 표현식도 분수 표기법중에 하나입니다. 요리책에 많이나오는 형태의 분수도 입력해보겠습니다.

$^1/_2$

```
^1/_2
```

### 괄호, 중괄호, 대괄호
LaTex에서 괄호를 사용하는 방법을 배워보겠습니다.

#### 소괄호

$(1+2)$

```
(1+2)
```

#### 중괄호

$\{1+2\}$

```
\{1+2\}
```

#### 대괄호

$[1+2]$

```
[1+2]
```

#### 자동 괄호 리사이즈
자동으로 괄호의 리사이즈가 되기 위해서는  "left", "right" 문자를 좌우로 넣어줍니다.

$\left(\frac{2}{3}\right)$

```
\left(\frac{2}{3}\right)
```

#### 수동 괄호 리사이즈
big, Big, bigg, Bigg 문자를 사용하면 수동으로 괄호 사이즈를 조절할 수 있습니다.

$\Bigg( \bigg( \Big( \big( ( ) \big) \Big) \bigg) \Bigg)$

```
\Bigg( \bigg( \Big( \big( ( ) \big) \Big) \bigg) \Bigg)
```

### 지수 / Power
승, 제곱에 해당하는 표기를 위해서 ^ 문자를 사용합니다.

$2^2=4$

```
2^2=4
```

### 순서 / Indices
각 아이템의 순서는 _ 문자로 표기합니다. _문자는 이후에 극한, 시그마, 적분표기 처럼 아래에 표기해야 하는 수식에서도 활용됩니다.

$a_1, a_2, a_3$

```
a_1, a_2, a_3
```

### 순서의 생략 /  dots
점을 출력하는 방법을 알아보겠습니다.
수와 수 사이에 값이 존재하는 상황에서 생략적 표기로 점을 많이 사용합니다.

$\dots$

```
\dots
```

가운데를 기준으로 점을 표기합니다.

$\cdots$

```
\cdots
```

새로로 점을 표기하는 방법입니다. 세로형태의 행렬, 매트릭스 내부에서 활용합니다.

$\vdots$

```
\vdots
```

대각선을 점을 표시하는 방법입니다. 행렬, 매트릭스를 표기할 때 대각선방향에 활용합니다.

$\ddots$

```
\ddots
```

### 루트(거듭제곱근) / Root
루트. square root의 약자로 sqrt 라고 사용합니다.

$\sqrt{2}$

```
\sqrt{2}
```

### 펙토리얼 / Factorial
!문자는 수학에서 팩토리얼을 뜻합니다.
3!이라는 뜻은 3,2,1 숫자로 만들수 있는 경우의 수 가 몇개인지를 뜻합니다.
3!은 (3,2,1),(3,1,2)(2,1,3)(2,3,1),(1,2,3)(1,3,2) 총 6개의 경우의 수가 존재합니다.
3x2x1=6 으로 계산했을때 결과와 경우의 수는 같습니다.

$n!$

$n! = 1 \times 2 \times 3 \times \ldots n$


펙토리얼을 Product 표기법을 사용해서 표현하면 아래와 같습니다.

$n! = \prod_{k=1}^n k$

### 집합 / Set
LaTex에서 집합의 표기법을 다루어 보겠습니다.

#### 합집합

$\{a,b,c\} \cup \{d,e\} = \{a,b,c,d,e\}$

```
\{a,b,c\} \cup \{d,e\} = \{a,b,c,d,e\}
```

#### 교집합
위 표기의 역표기.

$\{a,b,c\} \cap \{a,b,d\} = \{a,b\}$

```
\{a,b,c\} \cap \{a,b,d\} = \{a,b\}
```

#### 차집합
B-A=파이 공집함

#### 집합의 역
문자 위에 C 달린것

#### 포함된다
$x \in [-1,1]$

### 값의 비교 / Compare


### 삼각함수, 싸인, 코싸인, 탄젠트, 세타
$\cos (2\theta) = \cos^2 \theta - \sin^2 \theta$

### 파이 / Pi
$\pi$

$\Pi$

$\phi$


### 각도
90도

$90^\circ$

### 극한, limit
$\lim_{x \to \infty} \exp(-x) = 0$

### 시그마,for
$\sum_{i=1}^{10} t_i$

$\displaystyle\sum_{i=1}^{10} t_i$

### 로그 / log
```
\log_b a
```
### 미분 / differential
```
$\dv{Q}{t} = \dv{s}{t}$
```

### 적분 / integral
$\int_0^\infty \mathrm{e}^{-x}\,\mathrm{d}x$
$\int\limits_a^b$

### 행렬 / list

### 배열 / matrix
$A_{m,n} = 
 \begin{pmatrix}
  a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
  a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
  \vdots  & \vdots  & \ddots & \vdots  \\
  a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
 \end{pmatrix}$

### 벡터, 스칼라 / Vector, Scalar
$\overrightarrow{AB}$

$\overline{AB}$

### 선그리기

$\setlength{\unitlength}{3cm}
\begin{picture}(1,1)
\put(0,0){\line(1,0){1}}
\put(0,0){\line(0,1){1}}
\end{picture}$

### 좌표그리기
선을 그리는 방법을 응용하면 좌표를 그릴 수 있습니다. 또한 각진 도형들도 그릴 수 있습니다.

#### 원그리기

```
\setlength{\unitlength}{1mm}
\begin{picture}(60, 40)
\put(30,20){\circle{10}}
\end{picture}
```

### 벡터(화살표) 그리기
```
\setlength{\unitlength}{0.75mm}
\begin{picture}(60,40)
\put(30,20){\vector(1,0){30}}
\put(30,20){\vector(4,1){20}}
\put(30,20){\vector(3,1){25}}
\put(30,20){\vector(2,1){30}}
\put(30,20){\vector(1,2){10}}
\thicklines
\put(30,20){\vector(-4,1){30}}
\put(30,20){\vector(-1,4){5}}
\thinlines
\put(30,20){\vector(-1,-1){5}}
\put(30,20){\vector(-1,-4){5}}
\end{picture}
```

### 논문에 자주 나오는 기호
- 오메가 : \omega

#### LaTex 참고자료
아래 링크를 참고하시면 더 많은 LaTex정보를 보실 수 있습니다.

- LaTex 문법을 쉽게 익힐 수 있는 곳은 아래 사이트입니다.
	https://en.wikibooks.org/wiki/LaTeX/Mathematics

- LaTex를 이용해서 많은것을 그릴 수 있습니다. 아래 URL에서 구경해보세요.
	https://en.wikibooks.org/wiki/LaTeX/Picture


## WebTex
LaTex는 종이 인쇄물 기반의 기술입니다. 현대 과학의 대부분의 정보는 Web으로 표기됩니다.
WebTex 프로젝트는 LaTex를 html문서로 문제없이 컴파일 하는 것을 목표로 두고 있습니다.
문법은 LaTex와 거의 같습니다.
만약 여러분이 마크다운에서 WebTex 문법을 사용했다면 epub 파일을 제작할 때 아래 옵션을 추가해주면 됩니다.

	--webtex

WebTex 문법은 "$수식$" 형태로 구성되어 있습니다.

```
f(x)=\sum_{n=0}^\infty\frac{f^{(n)}(a)}{n!}(x-a)^n
```

위 문장이 문제없이 잘 처리되었다면 epub문서에 아래와 같은 수식이 그려집니다.

$f(x)=\sum_{n=0}^\infty\frac{f^{(n)}(a)}{n!}(x-a)^n$


#### 참고자료
- 프로젝트 사이트 : [http://pkgw.github.io/webtex/](http://pkgw.github.io/webtex/)
- 프로젝트 코드 : [https://github.com/pkgw/webtex/](https://github.com/pkgw/webtex/)

## MathML
Mathematical Markup Language의 약자입니다.
epub3 에서 수학기호를 표현하는 방법중 하나입니다.
XML 용용기술이며, HTML5 기술의 하나입니다.
개인적으로 LaTex문법이 짧고 함축적이고 가독성이 더 좋다고 생각합니다.
MathML은 여러분이 사용하는 브라우저가 지원할 수도 있고 지원하지 않을수도 있습니다.
브라우저에 따라 결과가 다를 수 있습니다.
파이어폭스, 사파리에서는 정상적으로 값이 출력되지만, 크롬에서는 아직 지원이 되지 않습니다.


#### MathML의 작성

![mathml_example](figures/mathml_example.png?raw=true)

2차방정식에 대한 근의 공식에 해당하는 MathML의 문법입니다.

    <math>
    <mi>x</mi>
    <mo>=</mo>
    <mfrac>
      <mrow>
      <mrow>
        <mo>-</mo>
        <mi>b</mi>
      </mrow>
      <mo>&PlusMinus;</mo>
      <msqrt>
        <msup>
        <mi>b</mi>
        <mn>2</mn>
        </msup>
        <mo>-</mo>
        <mrow>
        <mn>4</mn>
        <mo>&InvisibleTimes;</mo>
        <mi>a</mi>
        <mo>&InvisibleTimes;</mo>
        <mi>c</mi>
        </mrow>
      </msqrt>
      </mrow>
      <mrow>
      <mn>2</mn>
      <mo>&InvisibleTimes;</mo>
      <mi>a</mi>
      </mrow>
    </mfrac>
    </math>

xml 문법을 사용하기 때문에 많은 태그가 작성되어야 합니다.
일반적으로 LaTex 문법이 더 간단하기 때문에 
LaTex로 수식을 작성하고 MathML로 바꾸어주는 작업이 더 쉽습니다.

LaTex to MathML 컨버팅을 지원하는 사이트입니다.
- https://www.mathtowebonline.com

