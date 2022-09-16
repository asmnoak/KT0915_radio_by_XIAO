<p><H3>KT0915 DSPラジオICの評価</H3></p>
<p>
KT0915は、KTマイクロ製のFM/AM対応のDSPラジオICである。AMは中波、短波（32MHzまで）に対応している。<br>FMの周波数範囲は32MHzから110MHzと広い。<br>
SSOP16ピンの小さなパッケージであるため、変換基板にハンダ付けする必要がある。<br>
I2Cインターフェースでコントロールでき、Arduinoとの組み合わせが可能である。<br>
ただ電圧が3.3V対応なので、5VのArduinoと接続するためには信号レベルの電圧変換が必要である。<br>
ここでは、3.3Vで動作するSeeeduino XIAOと組み合わせて評価する。<br>
評価に使用したライブラリは、<a href="https://github.com/pu2clr/KT0915">こちら（pu2clr at GitHub）</a>にある。<br>
評価した構成はexamplesフォルダのKT0915_02_OLED（ArduinoProMini対応の回路図あり）である。<br>コードはKT0915_02_OLEDフォルダにあるものを改変した。<br>
概要、データシートは、<a href="https://www.aitendo.com/product/7449">こちら</a>を参考にするとよい。<br>
</p>

<p><strong>評価での対応</strong><br>
KT0915_02_OLEDの構成を変更して、周波数のUP/DOWNができるようにした。<br>
具体的には、コード上のD2、D3のロータリーエンコーダ（回路図にはない）の使用を止めて、バンドの切り替えに使用することにした。<br>回路図上のSW5、SW6に対応するコード（TEST_BUTTON1,2）を変更して、タクトスイッチで周波数のUP/DOWNができるようにした。<br>
</p>
<p><strong>H/W構成</strong><br>
 ・Seeeduino XIAO - コントローラ<br>
 ・SD1306 128x64 OLED表示装置<br>
 ・タクトスイッチ１から６<br>
  <ul>
   <li>タクトスイッチ１、２：D2,D3 - バンド切り替え</li>
   <li>タクトスイッチ３、４：D6,D7 - ボリューム</li>
   <li>タクトスイッチ５、６：D8,D9 - 周波数UP/DOWN</li>
   </ul>
 ・Xtal発振器（32768Hz）、コンデンサ類<br>
 ・I2C接続&nbsp; KT0915と表示装置（マルチドロップで接続）<br>
   &nbsp;&nbsp;&nbsp; 内蔵のプルアップ機能を利用しているのでプルアップ抵抗は不要<br>
</p>
<p>
<img src="./KT0915_OLED_XIAO.jpg" width="360" height="430">
FM 80.4MHzを受信中
</p>
<p><strong>操作</strong><br>
 ・バンド（中波、短波、FM）の変更（タクトスイッチ）。<br>
 ・音量調整（タクトスイッチ）。<br>
 ・受信周波数の変更（タクトスイッチ）。<br>
</p>
<p><strong>接続</strong><br>
各コンポーネントの接続は以下の通り。<br>
<p>
<table> 
<tr>
<td>I2C&nbsp;</td><td>XIAO</td>
</tr>
<tr>
<td>SCK</td><td>D5</td>
<tr>
<tr>
<td>SDA</td><td>D4</td>
<tr>
</table>
</p>
</p>
<p>
タクトスイッチ（ボタン）
<table> 
<tr>
<td>ボタン&nbsp;</td><td>XIAO&nbsp;</td>
</tr>
<tr>
<td>BAND</td><td>D2,D3</td>
</tr>
<tr>
<td>VOL</td><td>D6,D7</td>
</tr>
<tr>
<td>FREQ</td><td>D8,D9</td>
<tr>
</table>
</p>
<p><strong>インストール</strong><br>
<ol>
<li>コードを、ZIP形式でダウンロード</li>
<li>ArduinoIDEにおいて、ライブラリマネージャから以下を検索してインストールする</li>
 <ul>
  <li>KT0915</li>
  <li>Adafruit_BusIO</li>
  <li>Adafruit_GFX</li>
  <li>Adafruit_SSD1306</li>
 </ul>
<li>ArduinoIDEからKT0915_02_OLED.inoを開く</li>
<li>「検証・コンパイル」に成功したら、一旦、「名前を付けて保存」を行う</li>
</ol>
</p>
<p><strong>若干の解説</strong><br>
・受信バンドはakc_band band[]を変更する（行76）。<br>
・受信周波数の変更ついては、ボタンを押し続けると連続変更になる。<br>
・ENABLE（ピン9）は制御していないので、VCC（3.3V）に接続する。<br>
・VOL、CHピンは使用していない（試してみたが安定度がいまいちだった）。<br>
</p>
<p><strong>注意事項</strong><br>
・利用の際は、自己責任でお楽しみください。<br>
</p>
