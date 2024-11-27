java c
Statistics for HDS: Formative AssessmentGuidance (which will appear on the Part One assessment at the end of the module):   You   should   not   use   R   (or   other   statistical   software)   for this   assess-   ment,   except   as   a   very   basic   calculator   to   add   or   multiply   numbers   or   calculate   logs   and   exponentials.    Marks   are   available   for   partially   correct   answers.    Always   show your working when   performing   calculations,   so that   the   markers   can   see   how   much   you   have   understood.The   80th,   90th,   95th,   97.5th,   99th   and   99.9th   centiles   of   a   standard   normal   dis-   tribution   and   of   a   chi-square   distribution   with   1,   2,   3,   4   and   5   degrees   of freedom   (df)   are   given   in   the   following   table.

1.      Vitamin   D   plays   an   important   role   in   the   absorption   of   calcium   in   the   in-   testine.    In   a   study   of   the   association   between   calcium   and   vitamin   D,   the   levels   of   calcium   and   vitamin   D   were   measured   in   the   blood   serum   of   952   healthy   men. The   mean   calcium   level   in   the   sample   was   2.347   mmol/L   and   the mean vitamin D level was   82.91   nmol/L.   Using   a   linear   regression   model,   the   calcium   level (Y)   was   regressed   on   vitamin D   level (X). This    model   assumes   that
Y   ~ Normal(Q + βX;   σ2).
The   maximum   likelihood   estimate   of      (Q;   β)   was   calculated   to   be    (αˆ;   βˆ)      =
(2.058;   0.00348)   and   the   repeated   sampling   variance   matrix   was

(a)    Calculate the maximum likelihood estimate of the mean level   of calcium   in   people   whose   vitamin   D   level   is   70   nmol/L.
(b)    Calculate   the   standard   error   associated   with   this   maximum   likelihood   estimate.
(c)    Calculate   a   90%   Wald   conﬁdence   interval   for   the   mean   level   of calcium   in   people   whose   vitamin   D   level   is   70   nmol/L.
Note:   Iam asking you here   for the   Wald interval.   I   know that in Lecture   9   (on   Linear   Regression)   you   were   shown   how   to   calculate   conﬁdence intervals for Q and β based   on   t-distributions,   but I am   not   asking   you   to   do   that   here.    I want   to   test   your   understanding   of how   to   calculate   Wald   intervals.
(d)    Using   a   Wald   test,   test   the   null   hypothesis   that   β =   0   versus   the   alter-   native   hypothesis   that   β   ≠   0.      Show   your   working   carefully.Note:   I know   that in Lecture   9   (on Linear   Regression)   you   were   shown   how   to   perform   hypothesis   tests   based   on   t-distributions,   but   I   am   not   asking   you   to   do   that   here.    I want   you   to   use   a    Wald   test,   i.e.   a   test   based   on   the   normal   approximation.   I want   to   test   your understanding   of   how   to   do   that.
(e)      Apart   from   the   Wald   test   and   a   test   based   on   a   t-distribution,   suggest   one   other   way   that   this   null   hypothesis   could   be   tested.
2.    Suppose   Xi      ~ Exponential(λ)   (i =   1, . . . ,   n),   where   λ is   the   rate   parameter.
(a)    Derive   the   maximum   likelihood   estimate   λˆ of   λ   .
(b)    Derive   the   Fisher   Information   for   λ.
(c)    Use   the   Fisher   Information   to   calculate   the   asymptotic   standard   error of   λˆ.
(d)    代 写Statistics for HDS: Formative AssessmentR
代做程序编程语言  What   is   the   asymptotic   distribution   of   λˆ?
3.    A   researcher   collects   data   on   the   number   of   diagnoses   of   a   particular   rare   disease   in   Country   C   in   each   of   six   consecutive   years.    He   assumes   that   the   number   of diagnoses   in year   i has   a   Poisson   distribution with   mean   λ,   which   is   the   same   for   all   years   i   =   1, . . . ,   6.    He   also   assumes   that   the   numbers   of diagnoses   in   each   year   are   independent.    The   following   graph   shows   the   log   likelihood   function   for   these   data.
(a)      What   is   the   maximum   likelihood   estimate   of   λ?
(b)    Based   on   international   data   from   countries   with   a   similar   demography   to   Country   C,   it   is   thought   that   the   number   of   diagnoses   per   year   in   Country   C should be   around 3.5.    Perform. two diferent   tests   of the   null   hypothesis   that   λ = 3.5   versus   the   alternative   hypothesis   that   λ ≠   3.5.   For   each   of these   two   tests,   say   whether   you   reject   the   null   hypothesis,   and   report   the   two   p-values   as   accurately   as   you   can.
(c)    Using two   diferent   methods,   calculate two   95%   conﬁdence   intervals   for   λ   .
4. In this question, Iam trusting you not to use R. Using R to help you answer this question is cheating. However, if you really struggle to answer the question, then it is better that you experiment with R and see if that helps, rather than just giving up altogether. 
When   comparing   a   continuous   outcome   variable   in   two   groups,   e.g.   concen-   tration of some type of white blood cell   in   treated   and   untreated   individuals, two tests of the null hypothesis that the   average outcome in the   two   groups   is   the   same   are the t-test   and the Wilcoxon   rank   sum   test.   You   will   meet   both   of these   later   in   the   module.   The   following   R   code   can   be   used   to   perform   a   simulation   study   to   compare   the   powers   of these   two   tests.
M      <- 100000
a      <- rep(0, M)
b      <- rep(0, M)
set. seed(15465)
for      (m      in      1:M)    {
x    <- rnorm(n=10, mean=10, sd=3)
y    <- rnorm(n=10, mean=12, sd=3)
a[m]      <- t. test(x, y)$p . value
b[m]      <- wilcox. test(x, y)$p . value
}As you have probably guessed,t.   test(x,      y)$p   .   value and wilcox.   test(x,   y)$p   .   value   contain   the   p-values   from   the   t-test   and   Wilcoxon   test,   respec-   tively.
(a)      What      (one   or   two)   lines   of   R   code   would   you   add   to   this   program   in   order   to   make   it   report   the   powers   of the   two   size-0.05   tests?
(b)    Suppose   that   these      powers      are      29%      for   the      size-0.05   t-test      and      26%   for   the   size-0.05   Wilcoxon   test.    Explain   very   carefully   what   these   two   percentages   mean.
(c)    Explain   what   would   happen   to   these   two   powers   if the   lines
x    <- rnorm(n=10, mean=10, sd=3)
y    <- rnorm(n=10, mean=12, sd=3) in the above R code were changed to:i.                x    <- rnorm(n=10, mean=10, sd=3) y <- rnorm(n=10, mean=15, sd=3)ii.                x    <- rnorm(n=10, mean=10, sd=5) y <- rnorm(n=10, mean=12, sd=5)iii.                x    <- rnorm(n=10, mean=10, sd=3) y <- rnorm(n=10, mean=10, sd=3)




         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
