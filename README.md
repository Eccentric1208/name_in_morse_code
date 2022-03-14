const int LED = D7;
void setup() {
    pinMode(LED, OUTPUT);

}

void LongBlink(){
    digitalWrite(LED,HIGH);
    delay(1000);
    digitalWrite(LED, LOW);
    delay(500);
    
}
void shortBlink(){
    digitalWrite(LED,HIGH);
    delay(300);
    digitalWrite(LED,LOW);
    delay(500);
    
}

void loop() {
    int sequence[16]={1,1,1,0,1,1,1,0,1,0,0,0,0,0,0,0};
    for(int i=0;i<16;i++){
        if(sequence[i]==0)shortBlink();
        else LongBlink();
    }
    

}
