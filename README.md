const int led[] = {10,11};
int i;
int isLight = false;
void setup(){
  for (i = 0; i < 2; i++) {
  pinMode(led[i], OUTPUT); 
 }
}

void loop(){
  for (int i=0; i<2;i++) {
    if(( i + isLight) % 2 == 1)
    digitalWrite(led[i], HIGH);
    else
    digitalWrite(led[i], LOW);
  }
  isLight =!isLight;
  delay(500);
}


