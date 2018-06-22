# 床下空間の熱収支

![Sketch_of_Heat_Balance_of_Underfloor.jpg](Sketch_of_Heat_Balance_of_Underfloor.jpg)

集熱後の空気を供給する床下空間の熱収支式は、式(1)により表される。

$$
\begin{align*}
    \rho_{air}c_{P_{air}} V_{sa,d,t} \left( \theta_{sa,d,t} - \theta_{uf,d,t} \right) & \div 3600 \times 10^{3} + U_{bf} A_{s,ufvnt,A} \left( \theta_{g,d,t} - \theta_{uf,d,t} \right) + \alpha_{c,hse} A_{hse}  \left( \theta_{hse,d,t} - \theta_{uf,d,t} \right)\\
    &= \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} \left( \theta_{uf,d,t} - \theta_{ref,i,d,t} \right) + U_{bw} A_{bw} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right) + \psi L_{uf} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right)
\end{align*}
$$

<div style="text-align: right;"> (1) </div>

土間床を除いた床下蓄熱部位（基礎梁等）の熱収支式は、式(2)により表される。

$$
\begin{equation*}
    M_{hse}  \frac{\left( \theta_{hse,d,t} - \theta_{hse,d,t-1} \right)}{\Delta t} = \alpha_{c,hse} A_{hse} \left( \theta_{uf,d,t} - \theta_{hse,d,t} \right)
\end{equation*}
$$

<div style="text-align: right;"> (2) </div>

式(2)から、日付$d$の時刻$t$における土間床を除いた床下蓄熱部位（基礎梁等）の温度 $\theta_{hse,d,t}$ は、式(3)で与えられる。

<p style="text-indent:4em">式(2)⇔</p>

$$
\begin{align*}
     \left( \displaystyle \frac{M_{hse}}{\Delta t} +  \alpha_{c,hse} A_{hse} \right) \theta_{hse,d,t} =  \frac{M_{hse}}{\Delta t} \theta_{hse,d,t-1} +  \alpha_{c,hse} A_{hse} \theta_{uf,d,t}
\end{align*}
$$

<p style="text-indent:4em">　　⇔</p>

$$
\begin{align*}
     \theta_{hse,d,t} = \frac{\displaystyle \frac{M_{hse}}{\Delta t}}{\displaystyle \frac{M_{hse}}{\Delta t} +  \alpha_{c,hse} A_{hse}} \theta_{hse,d,t-1} + \frac{\alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} +  C_{uf-hse}} \theta_{uf,d,t}
\end{align*}
$$

<div style="text-align: right;"> (3) </div>

式(3)を式（1）に代入すると、式(1')を得る。

<p style="text-indent:4em">式(1)⇔</p>

$$
\begin{align*}
    \rho_{air}c_{P_{air}} V_{sa,d,t} \left( \theta_{sa,d,t} - \theta_{uf,d,t} \right) &\div 3600 \times 10^{3} + U_{bf} A_{s,ufvnt,A} \left( \theta_{g,d,t} - \theta_{uf,d,t} \right) + \alpha_{c,hse} A_{hse}  \left( \left\{ \frac{\displaystyle \frac{M_{hse}}{\Delta t}}{\displaystyle \frac{M_{hse}}{\Delta t} +  \alpha_{c,hse} A_{hse}} \theta_{hse,d,t-1} + \frac{\alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} + \alpha_{c,hse} A_{hse}} \theta_{uf,d,t} \right\} - \theta_{uf,d,t} \right) \\
    &= \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} \left( \theta_{uf,d,t} - \theta_{ref,i,d,t} \right) + U_{bw} A_{bw} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right) + \psi L_{uf} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right)
\end{align*}
$$

<p style="text-indent:4em">　　⇔</p>

$$
\begin{align*}
    \rho_{air}c_{P_{air}} V_{sa,d,t} \left( \theta_{sa,d,t} - \theta_{uf,d,t} \right) &\div 3600 \times 10^{3} + U_{bf} A_{s,ufvnt,A} \left( \theta_{g,d,t} - \theta_{uf,d,t} \right) + \frac{\displaystyle \frac{M_{hse} \alpha_{c,hse} A_{hse}}{\Delta t}}{\displaystyle \frac{M_{hse}}{\Delta t} +  \alpha_{c,hse} A_{hse}}  \left( \theta_{hse,d,t-1} - \theta_{uf,d,t} \right) \\
    &= \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} \left( \theta_{uf,d,t} - \theta_{ref,i,d,t} \right) + U_{bw} A_{bw} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right) + \psi L_{uf} \left( \theta_{uf,d,t} - \theta_{ex,d,t} \right)
\end{align*}
$$

<div style="text-align: right;"> (1') </div>

式(1')から、日付$d$の時刻$t$における床下温度 $\theta_{uf,d,t}$ は、式(4)で与えられる。

$$
\begin{equation*}
   \theta_{uf,d,t} = \displaystyle \frac{\rho_{air}c_{P_{air}} V_{sa,d,t} \theta_{sa,d,t} \div 3600 \times 10^{3} + \displaystyle \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} \theta_{ref,i,d,t} + U_{bw} A_{bw} \theta_{ex,d,t} + \psi L_{uf} \theta_{ex,d,t} + U_{bf} A_{s,ufvnt,A} \theta_{g,d,t} + \frac{\displaystyle \frac{M_{hse}}{\Delta t}\alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} + \alpha_{c,hse} A_{hse}} \theta_{hse,d,t-1}}{\rho_{air}c_{P_{air}} V_{sa,d,t} \div 3600 \times 10^{3} + \displaystyle \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} + U_{bw} A_{bw} + \psi L_{uf} + U_{bf} A_{s,ufvnt,A} + \frac{\displaystyle \frac{M_{hse}}{\Delta t} \alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} + \alpha_{c,hse} A_{hse}}}
\end{equation*}
$$

<p style="text-indent:2em">⇔</p>

$$
\begin{equation*}
   \theta_{uf,d,t} = \displaystyle \frac{\rho_{air}c_{P_{air}} V_{sa,d,t} \theta_{sa,d,t} + \left( \displaystyle \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} \theta_{ref,i,d,t} + U_{bw} A_{bw} \theta_{ex,d,t} + \psi L_{uf} \theta_{ex,d,t} + U_{bf} A_{s,ufvnt,A} \theta_{g,d,t} + \frac{\displaystyle \frac{M_{hse}}{\Delta t} \alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} + \alpha_{c,hse} A_{hse}} \theta_{hse,d,t-1} \right) \times 3.6}{\rho_{air}c_{P_{air}} V_{sa,d,t} + \left( \displaystyle \sum_{i=1}^{12} U_{s} A_{s,ufvnt,i} H_{ref,i,d,t} + U_{bw} A_{bw} + \psi L_{uf} + U_{bf} A_{s,ufvnt,A} + \frac{\displaystyle \frac{M_{hse}}{\Delta t} \alpha_{c,hse} A_{hse}}{\displaystyle \frac{M_{hse}}{\Delta t} + \alpha_{c,hse} A_{hse}} \right) \times 3.6}
\end{equation*}
$$

<div style="text-align: right;"> (4) </div>

ここで、

$A_{s,ufvent,A}$ : 暖冷房区画$i$において集熱後の空気を供給する床下空間に接する床の面積の合計((m<sup>2</sup>) <br/>
$A_{s,ufvent,i}$ : 暖冷房区画$i$において集熱後の空気を供給する床下空間に接する床の面積((m<sup>2</sup>) <br/>
$A_{bw}$ : 基礎外壁の面積(m<sup>2</sup>) <br/>
$A_{hse}$ : 土間床を除いた床下蓄熱部位の面積(m<sup>2</sup>) <br/>
$c_{P_{air}}$ : 空気の比熱(kJ/(kg $\cdot$ K)) <br/>
$H_{ref,d,t,i}$ : 日付$d$の時刻$t$における暖冷房区画$i$の温度係数(-) <br/>
$L_{uf}$ : 基礎外周長(m) <br/>
$M_{hse}$ : 土間床を除いた床下蓄熱部位の熱容量(J/K) <br/>
$U_{bf}$ : 土間床の熱貫流率(W/(m<sup>2</sup> $\cdot$ K)) <br/>
$U_{bw}$ : 基礎外壁の熱貫流率(W/(m<sup>2</sup> $\cdot$ K)) <br/>
$U_{s}$ : 床の熱貫流率(W/(m<sup>2</sup> $\cdot$ K)) <br/>
$V_{sa,d,t}$ : 日付$d$の時刻$t$における1時間当たりの床下または居室へ供給する空気の風量(m<sup>3</sup>/h) <br/>
$\alpha_{c,hse}$ : 土間床を除いた床下蓄熱部位の対流熱伝達率(W/(m<sup>2</sup> $\cdot$ K)) <br/>
$\Delta t$ : 計算タイムステップ(sec) <br/>
$\theta_{g,d,t}$ : 日付$d$の時刻$t$における地盤温度(℃) <br/>
$\theta_{ex,d,t}$ : 日付$d$の時刻$t$における外気温度(℃) <br/>
$\theta_{hse,d,t}$ : 日付$d$の時刻$t$における土間床を除いた床下蓄熱部位（基礎梁等）の温度(℃) <br/>
$\theta_{ref,d,t,i}$ : 日付$d$の時刻$t$における暖冷房区画$i$の参照室温(℃) <br/>
$\theta_{sa,d,t}$ : 日付$d$の時刻$t$において床下へ供給する空気の温度(℃) <br/>
$\theta_{uf,d,t}$ : 日付$d$の時刻$t$における床下温度(℃) <br/>
$\rho_{air}$ : 空気の密度(kg/m<sup>3</sup>) <br/>
$\psi$ : 基礎の線熱貫流率(W/(m $\cdot$ K))

である。
