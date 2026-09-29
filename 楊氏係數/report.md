<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"></script>
<script>
document.addEventListener("DOMContentLoaded", function() {
  renderMathInElement(document.body, {
    delimiters: [
      {left: "$$", right: "$$", display: true},
      {left: "$", right: "$", display: false}
    ],
    throwOnError: false
  });
});
</script>
</head>
<body>
</body>
</html>

<div class="cover-page">
  <div class="cover-main-title">
    普通物理學實驗
  </div>
  <div class="cover-subtitle">
    楊氏係數測定
  </div>
  <div class="cover-group">
    組別：第4組
  </div>
  <div class="cover-authors">
    組員：<br>
    <br>
    4115064204 林致齊<br>
    4115064201 洪秉寬<br>
    4115064213 胡庭睿<br>
  </div>
</div>

<style>
  .image-block {
    text-align: center;
    margin: 0 0 30px;
    break-inside: avoid;
    page-break-inside: avoid;
  }

  .image-box {
    display: table;
    margin: 0 auto;
    overflow: hidden;
    background-color: #f0f0f0;
    border-radius: 12px;
    line-height: 0;
  }

  .image-box img {
    width: auto;
    height: auto;
    max-width: 500px;
    max-width: min(500px, 100%);
    display: block;
    margin: 0 auto;
    border-radius: 12px;
  }

  .image-box.wide img {
    max-width: 100%;
  }

  .image-block figcaption {
    font-size: 16px;
    color: #555;
    margin-top: 4px;
  }

  /* PDF / 列印時固定使用 A4 */
  @page {
    size: A4;
    margin: 15mm 18mm;
  }

  .page-break {
    display: block;
    break-after: page;
    page-break-after: always;
  }

  /*
   * VS Code 預覽用：
   * 一張白色頁面寬度 = A4，灰色橫帶代表下一張 A4。
   * 因 Markdown 預覽本身不是排版軟體，所以頁高以人工分段控制。
   */
  @media screen {
    html {
      background: #d8d8d8 !important;
    }

    body {
      width: 210mm !important;
      max-width: 210mm !important;
      margin: 10mm auto !important;
      padding: 15mm 18mm !important;
      box-sizing: border-box !important;
      background: #ffffff !important;
      box-shadow: 0 0 8px rgba(0,0,0,0.22);
    }

    .page-break {
      height: 12mm;
      margin: 15mm -18mm;
      width: calc(100% + 36mm);
      background: #d8d8d8;
      border-top: 1px solid #bdbdbd;
      border-bottom: 1px solid #bdbdbd;
      box-sizing: border-box;
    }
  }

  @media print {
    .page-break {
      height: 0;
      margin: 0;
      border: 0;
      background: transparent;
    }
  }
</style>

<!-- 第2頁：實驗目的與原理 -->
<div class="page-break"></div>

## 實驗目的
因為金屬棒受力後的彎曲位移很小，本實驗希望學會利用光槓桿將微小位移放大到能由望遠鏡與米尺讀取的程度，並由實際量測到的載重與形變關係求出銅棒及鋼棒的楊氏係數。
另外，藉由更換不同寬度 $w$、厚度 $t$ 的鋼棒，觀察彎曲量與幾何尺寸的關係是否符合理論預測 $H\propto w^{-1}$、$H\propto t^{-3}$，並從實驗值與理論值的差異中分析尺寸量測、光槓桿放置與讀值操作可能造成的誤差，作為後續改進依據。
## 實驗原理
### 1. 應力、應變與楊氏係數
在彈性限度內，材料的應力與應變近似成正比：
\[
\frac{F}{A}=Y\frac{\Delta L}{L}
\tag{1}
\]
其中 $F/A$ 為應力、$\Delta L/L$ 為應變，比例常數 $Y$ 即楊氏係數。$Y$ 越大，代表材料在相同應力下越不易形變。
### 2. 橫樑彎曲
將長方形金屬棒架在相距 $L$ 的兩刀口上，於中央施加鉛直力 $G$。彎曲時上層受壓、下層受拉，中間存在長度近似不變的中性層。對矩形截面，可得中點撓度
\[
H=\frac14\left(\frac{L}{t}\right)^3\frac{1}{w}\frac{G}{Y}
=\frac{GL^3}{4Ywt^3}.
\tag{2}
\]
因此在材料、載重及其他條件固定時，
\[
H\propto w^{-1},\qquad H\propto t^{-3}.
\]
### 3. 光槓桿
金屬棒中點下降 $H$ 時，光槓桿鏡面轉動小角度 $\theta$。鏡面轉動 $\theta$ 時，反射光方向轉動約 $2\theta$。設光槓桿前後足垂直距離為 $a$，鏡面至米尺距離為 $d$，米尺像位移為 $h$，小角度近似下
\[
\frac{H}{a}\approx\theta,\qquad
\frac{h}{d}\approx2\theta,
\]
故
\[
H=\frac{ah}{2d}.
\tag{3}
\]
本實驗 $d=150$ cm、$a=2.4$ cm，因此位移放大倍率
\[
\frac{h}{H}=\frac{2d}{a}=125.
\]
<!-- 第3頁：計算原理與實驗方法 -->
<div class="page-break"></div>

### 4. 楊氏係數計算
將式 (3) 代入式 (2)，並令 $G=Mg$，得
\[
Y=\frac{MgL^3d}{2wt^3ah}.
\tag{4}
\]
實際計算時以無負荷狀態為基準：
\[
\Delta h_i=\bar h_i-\bar h_0,\qquad
\bar h_i=\frac{h_i+h_i'}{2},
\]
因此
\[
Y_i=\frac{M_i gL^3d}{2wt^3a\Delta h_i}.
\tag{5}
\]
若將 $\Delta h$ 對 $M$ 作線性擬合
\[
\Delta h=kM+b,
\]
則可由斜率 $k$ 求得
\[
Y=\frac{gL^3d}{2wt^3ak}.
\tag{6}
\]
本報告以式 (6) 的斜率法作為主要結果，式 (5) 的逐點結果用於檢查 $Y$ 是否隨負載改變。
## 實驗方法
1. 先量測兩刀口距離 $L$、光槓桿足距 $a$、鏡面至米尺距離 $d$，以及待測棒的寬度 $w$、厚度 $t$。
2. 將光槓桿後足置於金屬棒中央，以望遠鏡讀取米尺像。由 0 g 起每次增加 200 g 至 1000 g，再依序減重，將同一負載的加重與減重讀數取平均。
3. 以 $\Delta h=\bar h_i-\bar h_0$ 消除米尺零點與初始彎曲造成的固定偏移，並利用 $\Delta h-M$ 關係的斜率求楊氏係數。
4. 在幾何形狀實驗中固定材料、$M$、$L$、$a$、$d$，分別改變棒寬或棒厚，觀察 $\Delta h$ 與 $w$、$t$ 的冪次關係。
## 數據與結果
以下取
\[
g=980\ {\rm cm/s^2},\quad
a=2.4\ {\rm cm},\quad
d=150\ {\rm cm},\quad
L=34.6\ {\rm cm}.
\]
<!-- 第4頁：銅棒數據 -->
<div class="page-break"></div>

### 一、銅棒
銅棒尺寸：
\[
w=2.05\ {\rm cm},\qquad t=0.30\ {\rm cm}.
\]
$M_i$ (g)	加重 $h_i$ (cm)	減重 $h_i'$ (cm)	$\bar h_i$ (cm)	$\Delta h_i$ (cm)	$Y_i$ ($\times10^{11}$ dyne/cm²)
0	2.0	1.8	1.90	0	—
200	6.4	6.2	6.30	4.40	10.42
400	10.9	10.8	10.85	8.95	10.24
600	15.3	15.2	15.25	13.35	10.30
800	19.8	19.7	19.75	17.85	10.27
1000	24.4	24.5	24.45	22.55	10.16


逐點平均：
\[
\bar Y_{\rm Cu}=10.28\times10^{11}\ {\rm dyne/cm^2}.
\]
以 200 g 為例：
\[
Y=
\frac{200(980)(34.6)^3(150)}
{2(2.05)(0.30)^3(2.4)(4.40)}
=1.042\times10^{12}\ {\rm dyne/cm^2}.
\]
線性擬合為
\[
\Delta h=0.02250M-0.0667,\qquad R^2=0.99991.
\]
由斜率得
\[
\boxed{Y_{\rm Cu}=1.019\times10^{12}\ {\rm dyne/cm^2}=101.9\ {\rm GPa}}.
\]
<!-- 第5頁：鋼棒數據 -->
<div class="page-break"></div>

### 二、鋼棒
鋼棒尺寸：
\[
w=2.10\ {\rm cm},\qquad t=0.30\ {\rm cm}.
\]
$M_i$ (g)	加重 $h_i$ (cm)	減重 $h_i'$ (cm)	$\bar h_i$ (cm)	$\Delta h_i$ (cm)	$Y_i$ ($\times10^{11}$ dyne/cm²)
0	23.0	23.3	23.15	0	—
200	25.5	26.0	25.75	2.60	17.21
400	28.0	27.8	27.90	4.75	18.84
600	31.1	31.3	31.20	8.05	16.68
800	34.3	34.2	34.25	11.10	16.12
1000	37.0	37.0	37.00	13.85	16.15


逐點平均：
\[
\bar Y_{\rm steel}=17.00\times10^{11}\ {\rm dyne/cm^2}.
\]
線性擬合為
\[
\Delta h=0.014007M-0.2786,\qquad R^2=0.99663.
\]
由斜率得
\[
\boxed{Y_{\rm steel}=1.597\times10^{12}\ {\rm dyne/cm^2}=159.7\ {\rm GPa}}.
\]
<figure class="image-block">
  <div class="image-box"><img src="figures/fig1_dh_M.png" alt="Δh 對 M 圖"></div>
  <figcaption>圖 1　銅棒與鋼棒的總變化量 $\Delta h$ 對槽碼質量 $M$；實線為線性擬合。</figcaption>
</figure>

兩組數據均呈高度線性，表示在本實驗的負載範圍內，形變與負載近似成正比。
<!-- 第6頁：相鄰差與負載分析 -->
<div class="page-break"></div>

### 三、相鄰 200 g 的形變
每增加 200 g 時，相鄰平均讀數差為
區間 (g)	銅 $\Delta\bar h$ (cm)	銅 $Y'$ ($\times10^{11}$)	鋼 $\Delta\bar h$ (cm)	鋼 $Y'$ ($\times10^{11}$)
0→200	4.40	10.42	2.60	17.21
200→400	4.55	10.07	2.15	20.81
400→600	4.40	10.42	3.30	13.56
600→800	4.50	10.19	3.05	14.67
800→1000	4.70	9.75	2.75	16.27


<figure class="image-block">
  <div class="image-box"><img src="figures/fig2_inc_M.png" alt="相鄰差對 M 圖"></div>
  <figcaption>圖 2　每增加 200 g 時的米尺讀數變化。</figcaption>
</figure>

銅棒每增加 200 g 約改變 4.4～4.7 cm；鋼棒約 2.15～3.30 cm。鋼棒的局部變化較分散，因此相鄰差法對讀數波動較敏感。
<figure class="image-block">
  <div class="image-box"><img src="figures/fig3_Y_M.png" alt="Y_i 對 M_i 圖"></div>
  <figcaption>圖 3　逐點計算的 $Y_i$ 對 $M_i$。</figcaption>
</figure>

理論上同一材料的 $Y$ 不應隨負載改變。銅棒的 $Y_i$ 較集中；鋼棒在低負載處較分散，但 600 g 以上約落在 $16.1$～$16.7\times10^{11}$ dyne/cm²。
<!-- 第7頁：寬度分析 -->
<div class="page-break"></div>

### 四、鋼棒形變與寬度的關係
固定 $M=200$ g。
棒厚 $t$ (cm)	棒寬 $w$ (cm)	米尺讀數 $h_i$ (cm)	$\Delta h_i$ (cm)	$Y_i$ ($\times10^{11}$ dyne/cm²)
0.31	1.51	21.0	3.0	18.80
0.30	2.10	25.5	3.5	12.78
0.30	2.51	21.5	2.5	14.97
0.30	3.00	21.1	2.1	14.92


<figure class="image-block">
  <div class="image-box wide"><img src="figures/fig4_dh_w.png" alt="Δh 對 w 圖"></div>
  <figcaption>圖 4　$\Delta h$ 與棒寬 $w$ 的關係。</figcaption>
</figure>

以原始 4 點作乘冪擬合：
\[
\Delta h=4.20\,w^{-0.54},\qquad R^2=0.52.
\]
因此
\[
\beta_w=-0.54\quad\Rightarrow\quad \text{依講義規定取最接近整數為 }-1.
\]
但此組數據的 $R^2$ 僅 0.52，而且第一支棒的厚度為 0.31 cm、其他為 0.30 cm，因此只能說整體上呈現「棒越寬，彎曲量傾向減少」的趨勢，不能把本組數據視為對 $w^{-1}$ 的精確驗證。
<!-- 第8頁：厚度分析 -->
<div class="page-break"></div>

### 五、鋼棒形變與厚度的關係
固定 $M=200$ g。
棒寬 $w$ (cm)	棒厚 $t$ (cm)	米尺讀數 $h_i$ (cm)	$\Delta h_i$ (cm)	$Y_i$ ($\times10^{11}$ dyne/cm²)
2.50	0.18	64.5	14.5	12.00
2.50	0.22	29.7	3.4	28.03
2.51	0.30	21.5	2.5	14.97


<figure class="image-block">
  <div class="image-box wide"><img src="figures/fig5_dh_t.png" alt="Δh 對 t 圖"></div>
  <figcaption>圖 5　$\Delta h$ 與棒厚 $t$ 的關係。</figcaption>
</figure>

三點乘冪擬合得
\[
\Delta h=0.0420\,t^{-3.23},\qquad R^2=0.785.
\]
故
\[
\beta_t=-3.23\quad\Rightarrow\quad \text{依講義規定取最接近整數為 }-3.
\]
此結果的中央值接近理論預測 $-3$，但只有 3 個資料點，且 $t=0.22$ cm 的資料明顯偏離其他兩點，所以仍應保留量測不確定性的討論。
<!-- 第9頁：結果與討論 -->
<div class="page-break"></div>

## 結果與討論
### 1. $\Delta h$、$Y$ 與負載的物理意義
由式 (2) 可知，在材料及幾何尺寸固定時，
\[
\Delta h\propto M.
\]
因此 $\Delta h-M$ 圖應近似直線；相同的 200 g 增量所造成的 $\Delta\bar h$ 也應大致固定。若 $Y_i$ 隨 $M$ 沒有明顯趨勢，表示材料在量測範圍內仍近似線性彈性。
使用 $\Delta h=\bar h_i-\bar h_0$ 而非直接使用米尺絕對讀數 $h_i$，可以消除米尺零點、初始彎曲及固定預載造成的常數偏移。相鄰差法能直接檢查每增加 200 g 時的局部變化，但因每次形變量較小，較容易受到單次讀數波動影響；因此本報告以使用全部負載點的線性迴歸斜率作主要 $Y$ 值。
### 2. 棒寬與形變、楊氏係數
理論預測
\[
\Delta h\propto w^{-1}.
\]
本實驗得到 $\beta_w=-0.54$，取最接近整數為 $-1$，但 $R^2=0.52$，表示數據分散明顯。故結果只支持「寬度增加時形變大致減少」的定性趨勢，無法精確驗證 $w^{-1}$。
楊氏係數是材料性質，理論上不應隨棒寬改變。本組算出的 $Y$ 為 12.78～18.80 $\times10^{11}$ dyne/cm²，散布主要反映單次 200 g 量測及幾何尺寸量測誤差，而不是 $Y$ 真正隨寬度改變。
### 3. 棒厚與形變、楊氏係數
理論預測
\[
\Delta h\propto t^{-3}.
\]
實驗擬合得到 $\beta_t=-3.23$，最接近整數為 $-3$，與理論趨勢相符；但 $t=0.22$ cm 的資料使整體擬合分散較大。由於 $Y\propto t^{-3}$，厚度的量測誤差會被放大三倍，因此 $t$ 是本實驗中特別敏感的幾何量。
同樣地，$Y$ 理論上不應隨厚度改變。本組三筆 $Y$ 中，$t=0.22$ cm 所得 $28.03\times10^{11}$ dyne/cm² 與另外兩筆差異很大，較可能來自尺寸或位移讀值誤差，應以重複量測確認，而不宜直接刪除。
<!-- 第10頁：誤差與改進 -->
<div class="page-break"></div>

### 4. 與講義參考值比較及誤差來源
講義附表給出的參考範圍為：
- 銅：$12.3$～$12.9\times10^{11}$ dyne/cm²；
- 鋼：$19.5$～$20.6\times10^{11}$ dyne/cm²。
斜率法所得銅棒 $10.19\times10^{11}$、鋼棒 $15.97\times10^{11}$ dyne/cm²，分別比參考範圍中值低約 19% 與 20%。兩者都偏低，顯示除了隨機讀數波動外，可能仍存在共同的系統性偏差；但僅由本次數據無法確定是哪一個量造成。
可能的主要誤差來源如下：
1. 棒厚 $t$ 的量測：$Y\propto t^{-3}$，厚度只要有小幅誤差，就會明顯影響結果，因此量測位置與讀值精度都很重要。
2. 掛取槽碼時碰動光槓桿：掛、取槽碼時若碰到三腳架或鏡面，望遠鏡中的刻度變化就不完全是金屬棒彎曲造成的。
3. 望遠鏡與米尺讀值：重新對焦、十字線判讀、視差、桌面振動，以及槽碼尚未完全靜止，都可能造成讀值波動。
4. 換棒後光槓桿位置改變：每換一根鋼棒都必須重新放置光槓桿，後腳若未落在棒的中點，或前腳位置不同，都可能使量測條件改變。
5. 支點與負載位置：若刀口、吊盤或光槓桿後腳沒有位於理想位置，實際撓度會與理論模型略有差異。
6. 幾何尺寸實驗的量測次數較少：不同寬度與厚度的棒只有單次 200 g 量測，沒有完整的加重、減重與多點平均，因此重現性較差，這也是 $\beta_w$ 分散較大的可能原因。
若重新實驗，可用螺旋測微器在棒的不同位置多次量測厚度並取平均；量測 $a$ 時確認是後腳到兩前腳連線的垂直距離；掛取槽碼時避免碰動光槓桿，並等待裝置完全靜止後再讀值。幾何尺寸實驗也可對每支棒使用多個負載點、做加重與減重平均，再以線性迴歸求斜率。
<!-- 第11頁：結論與參考資料 -->
<div class="page-break"></div>

## 結論
1. 以光槓桿量測金屬棒彎曲，$\Delta h-M$ 呈高度線性；銅棒與鋼棒的 $R^2$ 分別為 0.99991 與 0.99663，支持本實驗負載範圍內近似線性彈性的假設。
2. 由線性擬合斜率求得\[
   Y_{\rm Cu}=1.019\times10^{12}\ {\rm dyne/cm^2}=101.9\ {\rm GPa},
   \]
   \[
   Y_{\rm steel}=1.597\times10^{12}\ {\rm dyne/cm^2}=159.7\ {\rm GPa}.
   \]
   兩者均比講義參考值低約 20%，表示實驗仍可能存在系統性偏差。
3. 厚度組得到 $\beta_t=-3.23$，與理論 $-3$ 的趨勢相符；寬度組得到 $\beta_w=-0.54$，雖取最接近整數為 $-1$，但因 $R^2$ 僅 0.52，只能視為定性支持。
4. 本實驗最需要注意棒厚量測、光槓桿放置與單次讀值的重現性。增加重複量測並使用更精密的厚度量具，可提升結果可靠度。
## 參考資料
1. 普通物理實驗講義，〈實驗三　楊氏係數測定〉。
2. D. Halliday, R. Resnick, J. Walker, Fundamentals of Physics, 10th ed., Ch. 12, “Equilibrium and Elasticity”.
3. W. D. Callister, Jr., D. G. Rethwisch, Materials Science and Engineering: An Introduction, 9th ed., Ch. 6, “Mechanical Properties of Metals”.
## 工作分配
組員	學號	負責工作
洪秉寬	4115064201	（請填寫）
胡庭睿	4115064213	（請填寫）
林致齊	4115064204	（請填寫）
