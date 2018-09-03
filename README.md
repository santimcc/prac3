
package javaapplication1;
import java.util.*;

public class JavaApplication1 {
    public static void imprimirMat (int[][]mtz){
        for (int i = 0; i < mtz.length; i++) {
            for (int j = 0; j < mtz[0].length; j++) {
                System.out.print(mtz[i][j] + "  ");                
            }
            System.out.println("");
        }
    }
    
    public static int[][] matrizRandom(int n, int m){
        int[][]matriz = new int[n][m];
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                matriz[i][j] = (new Random().nextInt(10));                
            }            
        }
        return matriz;
    }
        
    public static double promGeneral (int[][]mat){
        double suma = 0;
        for (int i = 0; i < mat.length; i++) {
            for (int j = 0; j < mat[0].length; j++) {
                suma = suma + mat[i][j];                
            }            
        }
        return (suma / (mat.length * mat[0].length));
    }
    
    public static int mejorNota(int[][]mat){
        int notamax = mat[0][2];
        for (int i = 0; i < mat[0].length; i++) {
            if (notamax < mat[i][2]){
                notamax = mat[i][2];
            }
            
        }
        return notamax;
    }
    
    public static int mejor1y6 (int[][]mat){
        int mejor = 0;
        for (int i = 0; i < mat.length; i++) {
            int[] is = mat[i];
            
        }
        return mejor;
    }
    
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.print("filas: ");
        int n = in.nextInt();
        System.out.print("columnas: ");
        int m =in.nextInt();
        
        int[][]mat = new int[n][m];
        
        if (n == m){
            System.out.println("Matriz cuadrada:");
            for (int i = 0; i < n; i++) {
                mat[i][i] = 1;                
            }
            imprimirMat(mat);
        }
        
        System.out.println("");
        System.out.println("");
        int[][]matrizR = matrizRandom(n,m);
        matrizR[3][2] = 15;
        imprimirMat(matrizR);
        System.out.println("promedio: " + promGeneral(matrizR));
        System.out.println("nota max en examen 3: " + mejorNota(matrizR));
        

        
    }
   
    
}
