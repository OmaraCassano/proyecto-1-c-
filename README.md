# proyecto-1-c-

#include <iostream>
#include <stdlib.h>
#include <time.h>

using namespace std;

void mostrarRefranIncompleto();
void mostrarRefranCompleto(); 
void obtenerRespuesta(); 
void compararRespuesta(); 
void mostrarSignificado(); 
void menuPrograma(); 

char Refran1[100] = {"En boca cerrada no entran moscas"};
char Refran2[100] = {"A palabras necias, oidos sordos"};
char Refran3[100] = {"A buen entendedor, pocas palabras bastan"};
char Refran4[100] = {"Zapateros a sus zapatos"};
char Refran5[100] = {"Visteme despacio que tengo prisa"};
char Refran6[100] = {"A quien madruga, Dios le ayuda"};
char Refran7[100] = {"A caballo regalado no le mires los dientes"};
char Refran8[100] = {"Piensa mal y acertara"};
char Refran9[100] = {"Al mal tiempo, buena cara"};
char Refran10[100] = {"Mas vale tarde que nunca"};

char PrimeraParte1[100] = {"En boca cerrada"};
char PrimeraParte2[100] = {"A palabras necias,"};
char PrimeraParte3[100] = {"A buen entendedor,"};
char PrimeraParte4[100] = {"Zapateros"};
char PrimeraParte5[100] = {"Visteme despacio"};
char PrimeraParte6[100] = {"A quien madruga,"};
char PrimeraParte7[100] = {"A caballo regalado"};
char PrimeraParte8[100] = {"Piensa mal"};
char PrimeraParte9[100] = {"Al mal tiempo,"};
char PrimeraParte10[100] = {"Mas vale tarde"};

char SegundaParte1[100] = {"no entran moscas"};
char SegundaParte2[100] = {"oidos sordos"};
char SegundaParte3[100] = {"pocas palabras bastan"};
char SegundaParte4[100] = {"a sus zapatos"};
char SegundaParte5[100] = {"que tengo prisa"};
char SegundaParte6[100] = {"dios le ayuda"};
char SegundaParte7[100] = {"no le mires los dientes"};
char SegundaParte8[100] = {"y acertara"};
char SegundaParte9[100] = {"buena cara"};
char SegundaParte10[100] = {"que nunca"};

char Significado1[100] = {"Callarse para prevenir errores."};
char Significado2[100] = {"Ignorar a aquello o a quienes no quieres escuchar porque no te aportan nada."};
char Significado3[100] = {"Si una persona es buena entendedora, no le hara falta darle muchas explicaciones."};
char Significado4[100] = {"Cada persona tienen algo que se le da bien, pues debera de atender a ello."};
char Significado5[200] = {"Cuando tienes prisa, no intentes hacer las cosas rapido porque te equivocaras y tendras que repetirlas."};
char Significado6[100] = {"Anima a una persona a madrugar con positividad porque podra ser mas productivo."};
char Significado7[100] = {"Cuando a una persona le regalan algo, no deberia de poner problemas."};
char Significado8[100] = {"Piensa mal sobre las personas y no te equivocaras."};
char Significado9[100] = {"Ante las adversidades, siempre hay que tener positividad."};
char Significado10[100] = {"Mejor ahora aunque sea tarde, que perderlo."};
char Frase[30];
int random, confirmacion = 0, negacion = 0;

int main(){
	int num;
	cout << "***************" << "\n";
	cout << "*                                         *" << "\n";
	cout << "*    Bienvenidos al juego de refranes:    *" << "\n";
	cout << "*                                         *" << "\n";
	cout << "***************" << "\n";
	
	do{
	    menuPrograma();
    	cin >> num;
    	mostrarRefranIncompleto();
    	obtenerRespuesta();
    	compararRespuesta();
	}while(num == 1);
	cout << "Gracias querido profesor Alvarado...";
	return 0;
}

void menuPrograma(){
	int num;
	cout << "Ingrese el numero de la opcion que desea utilizar: " << "\n";
	cout << "(1) Jugar a completar refranes." << "\n"; 
    cout << "(2) Mostrar resultados anteriores." << "\n"; 
    cout << "(3) Salir." << "\n";
    cout << "Ingrese el numero: " << "\n";
}

void mostrarRefranIncompleto(){
	
	srand(time(NULL));
    random = 0 + rand() % (10 - 1);
    if(random == 0){
    	cout << PrimeraParte1 << "\n";
	}
	else if(random == 1){
		cout << PrimeraParte2 << "\n";
	}
	else if(random == 2){
		cout << PrimeraParte3 << "\n";
	}
	else if(random == 3){
		cout << PrimeraParte4 << "\n";
	}
	else if(random == 4){
		cout << PrimeraParte5 << "\n";
	}
	else if(random == 5){
		cout << PrimeraParte6 << "\n";
	}
	else if(random == 6){
		cout << PrimeraParte7 << "\n";
	}
	else if(random == 7){
		cout << PrimeraParte8 << "\n";
	}
	else if(random == 8){
		cout << PrimeraParte9 << "\n";
	}
	else if(random == 9){
		cout << PrimeraParte10 << "\n";
	}
}

void obtenerRespuesta(){
	cout << "Ingresa la frase: ";
	cin >> Frase;
	cout << endl;
}

void compararRespuesta(){
	if(random == 0){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte1[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte1[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 1){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte2[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte2[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 2){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte3[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte3[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 3){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte4[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte4[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 4){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte5[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte5[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 5){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte6[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte6[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 6){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte7[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte7[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 7){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte8[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte8[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 8){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte9[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte9[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
	if(random == 9){
		for(int i = 0; i < 50; ++i){
			if(Frase[i] == SegundaParte10[i]){
				confirmacion = 1;
			}
			else if(Frase[i] != SegundaParte10[i]){
				negacion = 1;
			}
		}
		if(negacion == 1){
			cout << "Perdiste" << "\n";
		}
	}
}
