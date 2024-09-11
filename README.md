/*
Calibrar o Controle Remoto
Ligação: 5V ---> 5V
 GND ---> GND
 OUT --> Pino 3
*/
#include <IRremote.h> //inclui a Biblioteca
int RECV PIN = 3; // Pino que recebe o sinal
IRrecv irrec (RECV_PIN);
decode_results results;
void setup()
{
 Serial.begin(9600);
 irrecv.enableIRIn();
)
void loop()
{
 if (irrecv.decode(&results)) // Se receber algum sinal
 {
 Serial.println(results.value, HEX); //mostrar o sinal recebido
 irrecv.resume();
 ]
]
