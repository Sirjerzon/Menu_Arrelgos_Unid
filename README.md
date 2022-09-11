using System;

namespace Arrays
{
    class Program
    {
        static void Main(string[] args)
            
        { 
            string bufferstr ="" ;
   
            int opc;
            int buffer;
            int cant;
            int par;
            int imp;
            int[] list = new int[100];
            opc = 0;
            do
            {
                Console.Clear();
                Console.WriteLine("MENU DE ARREGLOS UNIDIMENSIONALES");
                Console.WriteLine("1. Ingresar valores al arreglo");
                Console.WriteLine("2. Imprimir valores del arreglo");
                Console.WriteLine("3. Imprimir el valor mas alto del arreglo");
                Console.WriteLine("4. Imprimir el valor mas bajo del arreglo");
                Console.WriteLine("5. Imprimir la suma total del arreglo");
                Console.WriteLine("6. Imprimir el arreglo al reves");
                Console.WriteLine("7. Imprimir pares e impares del arreglo");
                Console.WriteLine("8. Imprimir el cuadrado del arreglo");
                Console.WriteLine("9. Imprimir numeros primos del arreglo");
                Console.WriteLine("10. Salir");
                Console.WriteLine("Ingresar opcion del menu: ");
                opc = Convert.ToInt32(Console.ReadLine());

                switch (opc)
                {
                    case 1:
                        Console.WriteLine("¿Cuando valores desea ingresar?");
                        cant = Convert.ToInt32(Console.ReadLine());
                        Console.WriteLine("Ingresando valores al arreglo");
                        for (int i = 0; i < cant; i++) //0,1,2...7
                        {
                            Console.WriteLine("Ingrese un numero para la posición " + i);
                            list[i] = Convert.ToInt32(Console.ReadLine());
                        }
                        Console.WriteLine("Proceso finalizado...");
                        break;
                    case 2:
                        Console.WriteLine("Imprimiendo valores del arreglo");
                        for (int i = 0; i < list[i]; i++)
                        {
                            Console.WriteLine("Posición [" + i + "]: " + list[i]);
                        }
                        break;
                    case 3:
                        Console.WriteLine("Imprimiendo el valor mas alto del arreglo");
                        buffer = 0;
                        for (int i = 0; i < list[i]; i++)
                        {
                            if (list[i] > buffer)
                            {
                                buffer = list[i];
                            }
                        }
                        Console.WriteLine("El numero mayor es: " + buffer);
                        break;
                    case 4:
                        Console.WriteLine("Imprimiendo el valor mas bajo del arreglo");
                        buffer = 0;
                        for (int i = 0; i < list[i]; i++)
                        {
                            if (i == 0)
                            {
                                buffer = list[i];
                            }
                            else
                            {
                                if (list[i] < buffer)
                                {
                                    buffer = list[i];
                                }
                            }
                        }
                        Console.WriteLine("El numero menor es: " + buffer);
                        break;
                    case 5:
                        Console.WriteLine("Imprimiendo la suma total del arreglo");
                        buffer = 0;
                        for (int i = 0; i < list[i]; i++)
                        {
                            buffer = buffer + list[i];
                        }
                        Console.WriteLine("La suma del arreglo es: " + buffer);
                        break;
                    case 6:
                        Console.WriteLine("Imprimiendo el arreglo al reves");
                        for (int i = list.Length - 1; i >= 0; i--)
                        {
                            Console.WriteLine("Posicion [" + i + "]:" + list[i]);
                        }
                        break;
                    case 7:
                        Console.WriteLine("Imprimiendo resumen de pares e impares");
                        for (int i = 0; i < list[i]; i++)
                        {
                            if ((list[i] % 2) == 0)
                            {
                                par = list[i];
                                Console.WriteLine("Pares[" + i + "]:" + par);

                            }
                            else {
                                imp = list[i];
                                Console.WriteLine("Impares[" + i + "]:" + imp);
                            }
                        }
                        break;
                    case 8:
                        Console.WriteLine("Imprimiendo arreglo completo al cuadrado");
                        for (int i = 0; i < list[i]; i++)
                        {
                            double elevadoAlcuadrado = Math.Pow(list[i], 2);
                            Console.WriteLine("Cuadrado[" + i + "]:" + elevadoAlcuadrado);
                        }
                        break;

                    case 9:
                        bufferstr = "";
                        Console.WriteLine("Imprimiendo numeros primos");

                        
                        
                            for (int i = 0; i < list[i]; i++)
                        {
                      
                                if(EsPrimo(list[i]))
                                {
                                bufferstr = ((i == list.Length - 1) ? (bufferstr + list[i].ToString()) : (bufferstr + list[i] + ","));
                                }
                                   
                              
                                   

                                }
                        Console.WriteLine("Numeros primos del arreglo:"+bufferstr);



                        break;
                    case 10:
                        Console.WriteLine("Adios, gracias por usar el programa");
                        break;
                    default:
                        Console.WriteLine("Opps algo salio mal, ingrese una opcion de nuevo");
                        break;
                }
                Console.ReadKey();
            } while (opc !=10 );
        }
        static bool EsPrimo(int numero)
        {
            for (int i = 2; i < numero; i++)
            {
                if ((numero % i) == 0)
                {
                    
                    return false;
                }
            }

            
            return true;
        }
    }
    }

