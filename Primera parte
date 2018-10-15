# Proyecto-final


#include <math.h>
#include <stdio.h>
#include <iostream>

using namespace std;
//declaración de las funciones
void tiro_parabolico ();
void tiro_paraboconfri ();
void colisiones_movimiento ();
void colisiones_reposo ();
void rebotes ();
//variables necesarias para la funcion main
int a;
int b=0,c=0;
int main()
{
    
//ciclo mientras para el menu, se controla que no ingresen valores errados   
while (b!=1)
{
std::cout << "Bienvenido escoja una opcion" << std::endl;
std::cout << "1. Tiro Parabolico sin friccion" << std::endl;
std::cout << "2. Tiro Parabolico con friccion" << std::endl;
std::cout << "3. Colision elastica con particula en reposo" << std::endl;
std::cout << "4. Colision elastica con 2 particulas en movimiento" << std::endl;
std::cout << "5. Rebotes de una particula" << std::endl;
std::cout << "6. Salir" << std::endl;
std::cin >> a;
//se verifican que sean opciones entre 1 y 6
if ((a>0)&(a<7))
{
    // switch case para cada caso a calular
   switch(a)
    {
    //caso 1
     case 1: 
     std::cout << "Ejecutando proceso 1 ....." << std::endl;
     tiro_parabolico ();
     break;
    //caso 2 
     case 2:
     std::cout << "Ejecutando proceso 2 ....." << std::endl;
     tiro_paraboconfri ();
     break;
     //caso 3
     case 3:
     std::cout << "Ejecutando proceso 3 ....." << std::endl;
     colisiones_reposo();
     break;
   //caso 4
     case 4: 
     std::cout << "Ejecutando proceso 4 ....." << std::endl;
     colisiones_movimiento ();
     break;
   //caso 5
     case 5: 
     std::cout << "Ejecutando proceso 5 ....." << std::endl;
     rebotes ();
     break;
    //caso 6, opcion particular para salir del programa. 
     case 6: 
     std::cout << "Adios" << std::endl;
     b=1;
     break;
    }
    //control para salir o retornar al menu
    if ((a>0)&(a<6))
    { 
      c=0;
      std::cout << "Proceso terminado" << std::endl;
      while (c!=6)
      {
      //se solicita continuar o salir?
      std::cout << "Pesione 1 para volver al menu" << std::endl;
      std::cout << "Pesione 6 para salir" << std::endl;
      std::cin >> c;
      if (c==6)
      {
        std::cout << "Adios" << std::endl;
        b=1;   
      }
      //condición para identificar si la opcion seleccionada es errada
      else if (c!=1)
      {
        std::cout << "No es un valor permitido" << std::endl;  
      }
       if (c==1)
      {
        c=6;   
      }
      }
    }
}
//condición para identificar si la opcion seleccionada es errada o no en el menu principal
else
{
std::cout << "No es un valor permitido" << std::endl;
}   
}
    return 0;
}

// Fin de la funcion main





// Funcion para el tiro parabolico sin friccion
void tiro_parabolico()
{
float x,vx,t,y,y_0,v0y,v0,ang,v0x,xf,yf,vy;
float x0=0;
float ax=0;
float ay=9.8;

std::cout << "Ingresar el angulo" << std::endl;
std::cin >> ang;
std::cout << "Ingresar la posicion inicial de y" << std::endl;
std::cin >> y_0;
std::cout << "Ingresar la velocidad inicial" << std::endl;
std::cin >> v0;
std::cout << "Ingresar el tiempo" << std::endl;
std::cin >> t;

v0y=((v0*sin(ang)))*(57.29577951);
v0x=v0*cos(ang)*(57.29577951);
xf=((x0+(v0x*t))-((0.5)*(ax)*(t*t)));
yf=((y_0+(v0y*t))-((0.5)*(ay)*(t*t)));

std::cout <<"La posicion final de y es " <<yf << std::endl;
std::cout <<"La posicion final de x es " <<xf << std::endl;
std::cout <<"La velocidad en y es "<< v0y << std::endl;
std::cout <<"La velocidad en x es "<<v0x << std::endl;



}

//funcion para las colisiones en movimiento
void colisiones_movimiento()
{
//se declaran las variables necesarias   
float m1, m2, v01, v02, vf1, vf2;
//se solicitan las variables necesarias
std::cout << "Ingresar la masa 1" << std::endl;
std::cin >> m1;
std::cout << "Ingresar la masa 2" << std::endl;
std::cin >> m2;
std::cout << "Ingresar la velocidad de la masa 1" << std::endl;
std::cin >> v01;
std::cout << "Ingresar la velocidad de la masa 2" << std::endl;
std::cin >> v02;
//se realizan los calculos
vf1=(((m1-m2)/(m1+m2))*(v01))+(((2*m2)/(m1+m2))*(v02));
vf2=(((2*m1)/(m1+m2))*(v01))-((m1-m2)/(m1+m2))*(v02);

// impresion de los resultados
std::cout <<"La velocidad final de la masa 1 es "<< vf1 << std::endl;
std::cout <<"La velocidad final de la masa 2 es "<< vf2 << std::endl;
}//fin funcion para las colisiones en movimiento

//funcion para las colisiones con una de las masas en reposo
void colisiones_reposo ()
{ 
//se declaran las variables necesarias
float vf1;
float m1;
float m2;
float vf2;
float v01;
float v02;
//se solicitan los datos necesarios para ejecutar los calculos
std::cout << "Ingresar la masa 1" << std::endl;
std::cin >> m1;
std::cout << "Ingresar la masa 2" << std::endl;
std::cin >> m2;
std::cout << "Ingresar la velocidad de la masa 1" << std::endl;
std::cin >> v01;

//se calcular las velocidades
vf1=((m1-m2)/(m1+m2))*(v01);
vf2=((2*m1)/(m1+m2))*(v01);

//se imprimen los resultados
std::cout <<"La velocidad final de la particula 1 es " <<vf1 << std::endl;
std::cout <<"La velocidad final de la particula 2 es " << vf2 << std::endl;
}//fin funcion para las colisiones con una de las masas en reposo

// función para los rebotes de una particula
void rebotes ()
{
// se declaran las variables necesarias
float e1=0,h1,m1;
double Hn=0;
int n=1;
//se solicitan los datos necesarios
std::cout << "Ingresar la masa" << std::endl;
std::cin >>m1;
std::cout << "Ingresar la altura h" << std::endl;
std::cin >>h1;
//ciclo para controlar el ingreso del coeficiente de restitución, ya que debe cumplir 
//ciertos parametros entre 0 y 1
 do
 {
 std::cout << "Ingrese el coeficiente de restitución" << std::endl;
 std::cout << "El valor debe ser mayor que 0 y menor que 1" << std::endl;
 std::cin >>e1;
 }while(0>e1>1);
 //calculo de la altura despues de ada rebote
 do
 {
 Hn=((pow(e1,(2*n)))*h1);
 std::cout << "Altura despues del rebote numero "<<n<<" es = "<<Hn<< std::endl;
 n=n+1;
 }while(Hn>0);
 std::cout << "La particula reboto " <<(n-2)<<" veces "<< std::endl;
}//fin función para los rebotes de una particula

// funcion para el tiro parabolico con friccón
void tiro_paraboconfri ()
{
//declaración de los datos
float x,vx,t,y,y_0,v0y,v0,ang,v0x,xf,yf,vy,ti,r,k,m,inter,suminter=0;
float x0=0;
float ax=0;
float ay=0;
float g=9.8;
int ni=0,nicon=0;
//se solicitan los datos necesarios
std::cout << "Ingresar el angulo" << std::endl;
std::cin >> ang;
std::cout << "Ingresar la posicion inicial de y" << std::endl;
std::cin >> y_0;
std::cout << "Ingresar la velocidad inicial" << std::endl;
std::cin >> v0;
std::cout << "Ingresar el perido de tiempo" << std::endl;
std::cin >> t;
std::cout << "Ingresar el nuemero de intervalos" << std::endl;
std::cin >> ni;
std::cout << "Ingresar el valor de K (constante densidad y friccón)" << std::endl;
std::cin >> k;
std::cout << "Ingresar el radio de la particula" << std::endl;
std::cin >> r;
std::cout << "Ingresar la masa de la particula" << std::endl;
std::cin >> m;
//calculos para los intervalos
inter=(t/ni);
suminter=suminter+inter;
//se imprime los datos suministrados
std::cout <<"para los valores iniciales...  Angulo: " <<ang<<", Y0: "<<y_0<<", V0 "<<v0<< std::endl;
std::cout <<"perido de tiempo: " <<t<<", # de intervalos "<<ni<<", constante K: "<<k<< std::endl;
std::cout <<"Radio de particula: "<<r<< std::endl;

//ciclo mientras par realizar calculos por cada intervalo
while(suminter<=t)
{
ax=(-1)*((k*(v0*v0)*(r*r))/m)*(cos(ang));
ay=((-1)*((k*(v0*v0)*(r*r))/m)*(sin(ang)))-g;
//v0y=((v0*sin(ang)))*(57.29577951);
//v0x=v0*cos(ang)*(57.29577951);
//xf=((x0+(v0x*t))-((0.5)*(ax)*(t*t)));
//yf=((y_0+(v0y*t))-((0.5)*(ay)*(t*t)));
suminter=suminter+inter;
nicon=nicon+1;
//se imprimen los resultados
std::cout <<"Para el intervalo numero "<<nicon<<", Los resultados son:"<< std::endl;
std::cout <<"La acceleración "<<nicon<<" en y es: "<<ay<< std::endl;
std::cout <<"La acceleración "<<nicon<<" en x es: "<<ax << std::endl;
//std::cout <<"La posicion "<<nicon<<" en y es: "<<yf << std::endl;
//std::cout <<"La posicion "<<nicon<<" en x es: "<<xf << std::endl;
//std::cout <<"La velocidad "<<nicon<<" en y es: "<< v0y << std::endl;
//std::cout <<"La velocidad "<<nicon<<" en x es: "<<v0x << std::endl;
}
}//fin función para el tiro parabolico con friccón
