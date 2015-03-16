//# cizgi_izleyen_robot_kodu


int s1 = 2;
int s2 = 3;
int s3 = 4;
int s4 = 5;
int s5 = 6;
int s6 = 7;
int s7 = 8;
int s8 = 9;
int motor_sol = 10;
int motor_sag = 11;
int d1;
int d2;
int d3;
int d4;
int d5;
int d6;
int d7;
int d8;

void setup(){
Serial.begin(9600);

pinMode(13,OUTPUT);
pinMode(motor_sol,OUTPUT);
pinMode(motor_sag,OUTPUT);
pinMode(s1,INPUT);
pinMode(s2,INPUT);
pinMode(s3,INPUT);
pinMode(s4,INPUT);
pinMode(s5,INPUT);
pinMode(s6,INPUT);
pinMode(s7,INPUT);
pinMode(s8,INPUT);
digitalWrite(13,HIGH);
delay(30);
digitalWrite(13,LOW);
delay(1000);

}

void loop () {
  
Serial.println("devam");
d1=digitalRead(s1);
d2=digitalRead(s2);
d3=digitalRead(s3);
d4=digitalRead(s4);
d5=digitalRead(s5);
d6=digitalRead(s6);
d7=digitalRead(s7);
d8=digitalRead(s8);
delay(30);

if((d1==0)&&(d2==0)&&(d3==0)&&(d4==1)&&(d5==1)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,60);
analogWrite(motor_sag,60);
}
if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==1)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,65);
analogWrite(motor_sag,60);
}
if((d1==0)&&(d2==0)&&(d3==0)&&(d4==1)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,60);
analogWrite(motor_sag,65);
}

if((d1==0)&&(d2==0)&&(d3==1)&&(d4==1)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,65);
analogWrite(motor_sag,75);
}
if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==1)&&(d6==1)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,75);
analogWrite(motor_sag,65);
}

if((d1==0)&&(d2==0)&&(d3==1)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,65);
analogWrite(motor_sag,85);
}

if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==1)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,85);
analogWrite(motor_sag,65);
}

if((d1==0)&&(d2==1)&&(d3==1)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,70);
analogWrite(motor_sag,80);
}
if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==1)&&(d7==1)&&(d8==0))
{
analogWrite(motor_sol,80);
analogWrite(motor_sag,70);
}

if((d1==0)&&(d2==1)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,75);
analogWrite(motor_sag,100);
}

if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==1)&&(d8==0))
{
analogWrite(motor_sol,100);
analogWrite(motor_sag,75);
}
if((d1==1)&&(d2==1)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,75);
analogWrite(motor_sag,105);
}
if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==1)&&(d8==1))
{
analogWrite(motor_sol,105);
analogWrite(motor_sag,75);
}

if((d1==1)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==0))
{
analogWrite(motor_sol,60);
analogWrite(motor_sag,140);
}

if((d1==0)&&(d2==0)&&(d3==0)&&(d4==0)&&(d5==0)&&(d6==0)&&(d7==0)&&(d8==1))
{
analogWrite(motor_sol,140);
analogWrite(motor_sag,60);
}

}
