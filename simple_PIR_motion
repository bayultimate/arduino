nt outLedMerah = 13; //inisiasi lokasi pin merah yg merupakan penanda adanya gerakan
int outLedKuning = 12; //inisiasi lokasi pin kuning yg merupakan penanda loop sedang masuk LOW input signal (tidak ada gerakan)
int outLedHijau = 8; //inisiasi lokasi pin hijau yg merupakan penanda loop sedang masuk HIGH input signal (ada gerakan)
int inPir = 3; //inisiasi lokasi pin yg menerima input dari sensor

void setup() { 
  //inisiasi masing-masing pin mode, output untuk led, dan input untuk sensor PIR)
  pinMode(outLedMerah, OUTPUT);
  pinMode(outLedKuning, OUTPUT);
  pinMode (outLedHijau, OUTPUT);
  pinMode(inPir, INPUT);
  
  //hanya sekedar proses untuk menandakan led bekerja dengan baik sekaligus memberi waktu sensor untuk melakukan inisiasi awal
  digitalWrite(outLedMerah, HIGH); 
  digitalWrite(outLedKuning, HIGH);
  digitalWrite(outLedHijau, HIGH);
  delay(1000);
  digitalWrite(outLedMerah, LOW);
  digitalWrite(outLedKuning, LOW);
  digitalWrite(outLedHijau, LOW);
}

void loop() {
  
  if(digitalRead(inPir) == HIGH){ //cek apakah input sensor memberi signal high yang berarti ada gerakan
    digitalWrite(outLedMerah, HIGH); //hidupkan led merah
    digitalWrite(outLedHijau, HIGH); //hidupkan led hijau bersama dengan buzzer
    delay(50);
    digitalWrite(outLedHijau, LOW); //matikan led hijau
  }
  else {
    digitalWrite(outLedMerah, LOW); //matikan led merah
    digitalWrite(outLedKuning, HIGH); //hidupkan led kuning
    delay(50);
    digitalWrite(outLedKuning, LOW); //matikan led kuning
  }
}
