int pinA = 2; // przycisk wciśnięty -A
int pinB = 3; // przycisk wciśnięty -B

int led = 4; //Led

int sekA = 900;
int sztA = 5;
int sekB = 200;
int sztB = 10;

void setup() {
   pinMode(led, OUTPUT); //Dioda jako wyjście
  digitalWrite(led, LOW); //Wyłączenie diody
  pinMode(pinA, INPUT_PULLUP); //Przycisk jako wejście -A
  pinMode(pinB, INPUT_PULLUP); //Przycisk jako wejście -B

}

void loop() {
   if (digitalRead(pinA) == LOW) 
  for (int i = 0; i < sztA; i++){ //Jeśli przycisk wciśnięty -A
    digitalWrite(led, HIGH); //Włącz diodę
    delay(sekA); //Czekamy 10 sekund
    digitalWrite(led, LOW); //Wyłączamy diodę
    delay(sekA); //Czekamy 10 sekund
  }

     if (digitalRead(pinB) == LOW) 
  for (int i = 0; i < sztB; i++){ //Jeśli przycisk wciśnięty -B
    digitalWrite(led, HIGH); //Włącz diodę
    delay(sekB); //Czekamy 10 sekund
    digitalWrite(led, LOW); //Wyłączamy diodę
    delay(sekB); //Czekamy 10 sekund
  }

}
