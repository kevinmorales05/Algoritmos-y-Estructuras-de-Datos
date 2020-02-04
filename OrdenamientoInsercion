#include <iostream>

void ordenar(int *v,int);
void imprimir(int *v,int);
int *mezclar(int *A,int,int *B,int);
void buscar(int *C,int n,int num);

using namespace std;

int main(){
	int *A=new int[15];
	int *B=new int[15];
	int *C=new int[15];
	char resp='s',vec;
	int i=0,j=0;
	int num;
	
	cout<<"Dame los valores del vector A: "<<endl;
	while(resp=='s'||resp=='S'){
		cin>>A[i++];
		cout<<endl<<"Deseas agregar otro? s/n: "<<endl;
		cin>>resp; 
	}
	resp='s';
	cout<<"Dame los valores del vector B: "<<endl;
	while(resp=='s'||resp=='S'){
		cin>>B[j++];
		cout<<endl<<"Deseas agregar otro? s/n: ";
		cin>>resp; 
	}
	cout<<endl<<"Ordenando A"<<endl;
	ordenar(A,i);
	cout<<"Ordenando B"<<endl;
	ordenar(B,j);
	cout<<endl<<"Vector ordenado A:";
	imprimir(A,i);
	cout<<endl<<"Vector ordenado B:";
	imprimir(B,j);
	cout<<endl<<"Imprimiendo vector mezclado ordenado";
	C=mezclar(A,i,B,j);
	ordenar(C,i+j);
	imprimir(C,i+j);
	cout<<endl<<"Que vector quieres imprimir A,B,C: ";
	cin>>vec;
	if(vec=='A'){
		imprimir(A,i);
	}
	if(vec=='B'){
		imprimir(B,j);
	}
	if(vec=='C'){
		imprimir(C,i+j);
	}
	cout<<endl<<"Dame un numero para buscarlo en el vector C:"<<endl;
	cin>>num;
	buscar(C,i+j,num);
	return 0;
}

void ordenar(int *v,int n){
	int i,j,aux,minimo;
	for(i=0;i<n;i++){
		minimo=i;
		for(j=i+1;j<n;j++){
			if(v[j]<v[minimo]){
				minimo=j;
			}
		}
		aux=v[minimo];
		v[minimo]=v[i];
		v[i]=aux;
	}
}

void imprimir(int *v,int n){
	cout<<endl;
	for(int i=0;i<n;i++){
		cout<<v[i]<<" ";
	}
}

int *mezclar(int *A,int m,int *B,int n){
	int *C=new int[m+n];
	int i,j,k=0;
	for(i=0;i<m;i++){
		C[i]=A[i];
	}
	for(j=i;k<n;j++){
		C[j]=B[k++];
	}
	return C;
}

void buscar(int *C,int n,int num){
	int i,band=0;
	for(i=0;i<n;i++){
		band=0;
		if(C[i]==num){
			band=1;
			cout<<endl<<"Se encuentra en la posicion "<<i+1<<" el num "<<num;
			break;
		}
	}
	if(band==0){
		cout<<endl<<"No existe el numero buscado en el vector C";
	}
}
