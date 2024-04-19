Bu projede 7-30v arası, 30A kadar olan DC motorların STM32, Ardunio, Raspberry Pi ve PLC gibi cihazlar ile kontrol edilmesi ve ayrıca istenilen durumlarda, anahtar ve potansiyometre yardımı ile manuel kontol edilebilmesi amaçlanmıştır.
Bu devrenin şematik ve pcb tasarımı Altium Designer programı ile tamamlanıp, JLCPCB tarafından üretimi yapılmıştır. Devrenin şematik tasarımı oluşturulurken LTspice ve Breadboard üzerinden simule edilerek yapılmıştır. Pcb tasarımıda ise gerekli iz, via, bakır kalınlığı gibi etkenler Saturn PCB Designer programı kullanılarak hesaplanmıştır. 

Devre 7-30v arası gerilim ile çalışıp In1, Dır1 ve In2, Dır2 girişlerine ayrıca mcu kartları içinde 5v güç çıkışına sahiptir. In girişi ile motorun hızı. Dır girişi ilede motorun yön kontrolu yapılmaktadır. In sinyali 1.8, 2.5, 3.3 ve 5V gerilimler ile kontrol edilebilir. Gerekli logic tasarımı Karnaugh diagramı ile yapılmıştır. Pcb üzerindeki S1 ve S2 anahtarları giriş kısmında ki In1 ve In2 girişlerini iptal eder ve devre üzerinde ki NE555 entegresine ile bir PWM sinyal üretir. Bu sinyalin genliği ise devrede ki POT girişine bir potansiyometre bağlanarak kontrol edilir. Diğer SD1 ve SD2 anahtarları ile Motor yön kontrolu manuel olarak gerçekleştirilebilir.

Devre de Low side da N kanal IRF3205, High side da P kanal IRF4905 mosfetleri kullanılmıştır. High side da P kanal mosfet kullanılmasının sebebi ekstra BOOTSTRAP entegresi kullanmamak içindir. Mosfetleri sürmek için Push Pull yöntemi uygulanmıştır. Bu yöntemin uygulanma amacı Mosfetin saturasyon bölgesinde daha az kalması ve mosfetin daha hızlı bir şekilde kesime gitmesi amaçlanmıştır. Mosfet bu yöntem sayesinde daha hızlı anahatarlama yapabilmektedir.

![43222](https://github.com/sezear07/DC-MOTOR-TEST-KARTI/assets/167361624/04e55ebd-b8c6-4401-bb7b-b4f7ba68e1c4)
Şematik Tasarım
![54545444](https://github.com/sezear07/DC-MOTOR-TEST-KARTI/assets/167361624/4ef15740-ecf6-450b-aeee-dc7c3cd8e112)

Gerekli PCB tasarımı kullanım kolaylığı amaçlanarak tasarlanmıştır ve EMI den etkilenmesi muhtemel parçaların konum ve yol dizaynına dikkat edilmiştir.
![gdfgfff](https://github.com/sezear07/DC-MOTOR-TEST-KARTI/assets/167361624/37c96adb-9878-4c74-8721-a267e44538cf)
![kjnhhjkjuhuhjvbglfcukhvgfukjytgv](https://github.com/sezear07/DC-MOTOR-TEST-KARTI/assets/167361624/41e348a6-8798-4eac-b7f1-3fea309881bb)
