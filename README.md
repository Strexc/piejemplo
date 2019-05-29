#Ejemplo de una pila en Java basic.

Metodos de clase.
```java
public class PilaEnt {
    
    public int tope;
    public int [] elements;
    public int tam; 
    
   //Contrustores
    public PilaEnt(){
        tope = 0;
        elements = new int [1];
        tam = 0;
    }
    
    public PilaEnt(int tam)
    {
        tope = tam;
        elements = new int [tam];
        this.tam = tam;
    }
    //Metodos
    public void anular()
    {
        tope = tam;
        System.out.println("Se elimaron los daros de la pila");
    }
    
    public boolean esta_vacia()
    {
        if(tope > tam-1)
            return true;
        else
            return false;
    }
    
    public Integer regresar_tope(){
       if(esta_vacia()==true){
           System.out.println("ERROR: La pila esta vacia");
           return null;
       }
       else{
           return(elements[tope]);
       }
    }
    
    public void sacar(){
        if(esta_vacia()==true)
        {
            System.out.println("ERROR: La pila esta vacia");  
        }
        else{
            tope = tope + 1;
        }   
    }
    
    public void meter(int x){
        
        if(tope == 0)
        {
            System.out.println("ERROR: La pila esta llena"); 
        }
        else
        {
            tope = tope - 1;
            elements[tope]=x;
        }
    }  
}
```
