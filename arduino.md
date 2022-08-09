#define LED_B 4
#define LED_G 14
#define LED_R 12
void setup() {
// put your setup code here, to run once:
Serial.begin(9600);
pinMode(LED_B, OUTPUT);
pinMode(LED_G, OUTPUT);
pinMode(LED_R, OUTPUT);

}
int count=0;
void loop() {
// put your main code here, to run repeatedly:
/\*digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
(1000);
digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,HIGH);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,LOW);
digitalWrite(LED_G,HIGH);
digitalWrite(LED_R,LOW);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,LOW);
digitalWrite(LED_G,HIGH);
digitalWrite(LED_R,HIGH);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,HIGH);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,HIGH);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,HIGH);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,HIGH);
digitalWrite(LED_G,HIGH);
digitalWrite(LED_R,LOW);
delay(1000);

digitalWrite(LED_B,LOW);
digitalWrite(LED_G,LOW);
digitalWrite(LED_R,LOW);
delay(1000);
digitalWrite(LED_B,HIGH);
digitalWrite(LED_G,HIGH);
digitalWrite(LED_R,HIGH);
delay(1000);
*/
/*Serial.println(analogRead(A0));
//count++;
//if(count==11){
// count=0;
//}
delay(100);
if(analogRead(A0)){
digitalWrite(LED_R,LOW);
}\*/
if(Serial.available()>0){
char RxD=Serial.read();
if(RxD=='0'){
digitalWrite(LED_B,LOW);
digitalWrite(LED_R,LOW);
digitalWrite(LED_G,LOW);

    }
    else if(RxD=='1'){
      digitalWrite(LED_B,HIGH);
      digitalWrite(LED_G,HIGH);
      digitalWrite(LED_R,HIGH);
    }

}
}
