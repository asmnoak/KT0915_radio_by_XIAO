<p><H3>KT0915 DSP���W�IIC�̕]��</H3></p>
<p>
KT0915�́AKT�}�C�N������FM/AM�Ή���DSP���W�IIC�ł���BAM�͒��g�A�Z�g�i32MHz�܂Łj�ɑΉ����Ă���B<br>FM�̎��g���͈͂�32MHz����110MHz�ƍL���B<br>
SSOP16�s���̏����ȃp�b�P�[�W�ł��邽�߁A�ϊ���Ƀn���_�t������K�v������B<br>
I2C�C���^�[�t�F�[�X�ŃR���g���[���ł��AArduino�Ƃ̑g�ݍ��킹���\�ł���B<br>
�����d����3.3V�Ή��Ȃ̂ŁA5V��Arduino�Ɛڑ����邽�߂ɂ͐M�����x���̓d���ϊ����K�v�ł���B<br>
�����ł́A3.3V�œ��삷��Seeeduino XIAO�Ƒg�ݍ��킹�ĕ]������B<br>
�]���Ɏg�p�������C�u�����́A<a href="https://github.com/pu2clr/KT0915">������ipu2clr at GitHub�j</a>�ɂ���B<br>
�]�������\����examples�t�H���_��KT0915_02_OLED�iArduinoProMini�Ή��̉�H�}����j�ł���B<br>�R�[�h��KT0915_02_OLED�t�H���_�ɂ�����̂����ς����B<br>
�T�v�A�f�[�^�V�[�g�́A<a href="https://www.aitendo.com/product/7449">������</a>���Q�l�ɂ���Ƃ悢�B<br>
</p>

<p><strong>�]���ł̑Ή�</strong><br>
KT0915_02_OLED�̍\����ύX���āA���g����UP/DOWN���ł���悤�ɂ����B<br>
��̓I�ɂ́A�R�[�h���D2�AD3�̃��[�^���[�G���R�[�_�i��H�}�ɂ͂Ȃ��j�̎g�p���~�߂āA�o���h�̐؂�ւ��Ɏg�p���邱�Ƃɂ����B<br>��H�}���SW5�ASW6�ɑΉ�����R�[�h�iTEST_BUTTON1,2�j��ύX���āA�^�N�g�X�C�b�`�Ŏ��g����UP/DOWN���ł���悤�ɂ����B<br>
</p>
<p><strong>H/W�\��</strong><br>
 �ESeeeduino XIAO - �R���g���[��<br>
 �ESD1306 128x64 OLED�\�����u<br>
 �E�^�N�g�X�C�b�`�P����U<br>
  <ul>
   <li>�^�N�g�X�C�b�`�P�A�Q�FD2,D3 - �o���h�؂�ւ�</li>
   <li>�^�N�g�X�C�b�`�R�A�S�FD6,D7 - �{�����[��</li>
   <li>�^�N�g�X�C�b�`�T�A�U�FD8,D9 - ���g��UP/DOWN</li>
   </ul>
 �EXtal���U��i32768Hz�j�A�R���f���T��<br>
 �EI2C�ڑ�&nbsp; KT0915�ƕ\�����u�i�}���`�h���b�v�Őڑ��j<br>
   &nbsp;&nbsp;&nbsp; �����̃v���A�b�v�@�\�𗘗p���Ă���̂Ńv���A�b�v��R�͕s�v<br>
</p>
<p>
<img src="./KT0915_OLED_XIAO.jpg" width="360" height="430">
FM 80.4MHz����M��
</p>
<p><strong>����</strong><br>
 �E�o���h�i���g�A�Z�g�AFM�j�̕ύX�i�^�N�g�X�C�b�`�j�B<br>
 �E���ʒ����i�^�N�g�X�C�b�`�j�B<br>
 �E��M���g���̕ύX�i�^�N�g�X�C�b�`�j�B<br>
</p>
<p><strong>�ڑ�</strong><br>
�e�R���|�[�l���g�̐ڑ��͈ȉ��̒ʂ�B<br>
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
�^�N�g�X�C�b�`�i�{�^���j
<table> 
<tr>
<td>�{�^��&nbsp;</td><td>XIAO&nbsp;</td>
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
<p><strong>�C���X�g�[��</strong><br>
<ol>
<li>�R�[�h���AZIP�`���Ń_�E�����[�h</li>
<li>ArduinoIDE�ɂ����āA���C�u�����}�l�[�W������ȉ����������ăC���X�g�[������</li>
 <ul>
  <li>KT0915</li>
  <li>Adafruit_BusIO</li>
  <li>Adafruit_GFX</li>
  <li>Adafruit_SSD1306</li>
 </ul>
<li>ArduinoIDE����KT0915_02_OLED.ino���J��</li>
<li>�u���؁E�R���p�C���v�ɐ���������A��U�A�u���O��t���ĕۑ��v���s��</li>
</ol>
</p>
<p><strong>�኱�̉��</strong><br>
�E��M�o���h��akc_band band[]��ύX����i�s76�j�B<br>
�E��M���g���̕ύX���ẮA�{�^��������������ƘA���ύX�ɂȂ�B<br>
�EENABLE�i�s��9�j�͐��䂵�Ă��Ȃ��̂ŁAVCC�i3.3V�j�ɐڑ�����B<br>
�EVOL�ACH�s���͎g�p���Ă��Ȃ��i�����Ă݂�������x�����܂����������j�B<br>
</p>
<p><strong>���ӎ���</strong><br>
�E���p�̍ۂ́A���ȐӔC�ł��y���݂��������B<br>
</p>
