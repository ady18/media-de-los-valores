# media-de-los-valores

package com.ejercicio.array;
import java.util.*;

public class Ejercicio_1 {

	public static void main(String[] args) {
		
		/*Programa Java que lea por teclado 10 números enteros y los guarde en un array. 
		 * A continuación calcula y muestra por separado la media de los valores positivos 
		 * y la de los valores negativos.
		 */

		Scanner sc = new Scanner(System.in);
		int [] array = new int[10];
		int positivo = 0, negativo = 0;
		int sumaPositivo = 0, sumaNegativo = 0;
		
		//Para la lectura del array
		for(int i=0; i<10;i++){
			
			System.out.print("numeros [" + i + "] = ");
			array[i] = sc.nextInt();
		}
		
		//Para recorrer la matriz y sumar los positivos y negativos
			for(int j=0;j<10;j++){
				if(array[j]>0){
					
					sumaPositivo += array[j];
					positivo++;
					
				} else if(array[j]<0){
					sumaNegativo += array[j];
					negativo++;
				}
			}
		
		//Para calcular y mostrar medias
		if(positivo!=0){
			
			System.out.println("La media de los valores positivos: " + (sumaPositivo/positivo));
		} else{
			
			System.out.println("No se ha introducido numeros positivos");
		}
		
		if(negativo!=0){
			
			System.out.println("La media de los valores negativos: " + (sumaNegativo/negativo));
		}else{
			
			System.out.println("No se ha introducido numeros negativos");
		}
	}

}
