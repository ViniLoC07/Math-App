# Math-App
um aplicativo simples que resolve boa parte das fórmulas matemáticas ensinadas no ensino médio das escolas brasileira. (é um projeto apenas para minha aprendizagem na linguagem c#)

using System;
using System.Linq;

namespace Console_Math
{
	public static class Program
	{   	
		public static void Main()
		{		 

          Console.WriteLine("Escolha qual função deseja utilizar:");
          Console.WriteLine("-1 Teorema de Pitagoras");
          Console.WriteLine("-2 Vertice da Parabola");
          Console.WriteLine("-3 Baskaras");
          Console.WriteLine("-4 Porcentagem");
          Console.WriteLine("-5 Area de Figuras Planas");

          int escolha = int.Parse(Console.ReadLine());
          
              switch (escolha)
              {
        	      case 1:
                     TeoremaPitagoras();
                  break;
                  
                  case 2:
                     VerticeParabola();
                  break;
                  
                  case 3:
                     Bhaskara();
                  break;
                  
                  case 4:
                     Porcentagem();
                  break;

                  case 5:
                     GeomPlana();
                  break;

                  /*case 6:
                     Porcentagem();
                  break;

                  case 7:
                     Porcentagem();
                  break;
                  */
                  default:
                     Console.WriteLine("Escolha uma opção valida!");
                     Main();
                  break;                  
              }          
		}
  
	    static void TeoremaPitagoras()
		{
			
      Console.WriteLine("Digite o valor de A:");
			double A = double.Parse(Console.ReadLine());
			Console.WriteLine("Digite o valor de B:");
			double B = double.Parse(Console.ReadLine());

			double Quad_A = Math.Pow(A, 2);
			double Quad_B = Math.Pow(B, 2);

			double C = Math.Sqrt(Quad_A + Quad_B);
			 
			Console.WriteLine($"Seu C é igual a {C:F3}");
			Console.WriteLine();
			Console.WriteLine();
			Main();
	    }
	    
	    static void VerticeParabola()
	    {   
	    Console.WriteLine("Digite o valor de A:");
			double a = double.Parse(Console.ReadLine());
			Console.WriteLine("Digite o valor de B:");
			double b = double.Parse(Console.ReadLine());
      Console.WriteLine("Digite o valor de C:");
			double c = double.Parse(Console.ReadLine());

			double multi = 4 * a * c;

			double Quad_Bd = Math.Pow(b, 2);
			double Delta = Quad_Bd - multi;			

			double VerticeParabola = Delta / 4 * a;

			//Console.WriteLine(Delta);

			Console.WriteLine("Seu Vertice é " + VerticeParabola);
			Console.WriteLine();
			Console.WriteLine();
			Main();
	    }	 
		
		static void Bhaskara()
		{
      Console.WriteLine("Digite o valor de A:");
			double a = double.Parse(Console.ReadLine());
			Console.WriteLine("Digite o valor de B:");
			double b = double.Parse(Console.ReadLine());
			Console.WriteLine("Digite o valor de C:");
			double c = double.Parse(Console.ReadLine());

			double Delta = (b * b) - (4 * a * c);

			double raizDelta = Math.Sqrt(Delta);
			double ResulDenominador = -b + raizDelta;
			double Calc_Soma = ResulDenominador / (2*a);			
			double ResulDenominador2 = -b - raizDelta;
			double Calc_Subt = ResulDenominador2 / (2*a);			

			Console.WriteLine("Resultado para x1(Somando): " + Calc_Soma);
			Console.WriteLine("Resultado para x2 (Subtração): " + Calc_Subt);
			Console.WriteLine();

			Main();
		}
  
		static void Porcentagem()
		{
			Console.WriteLine("Qual função deseja utilizar?");
			Console.WriteLine();
      Console.WriteLine("-1 Valor equivalente a uma porcentagem");
			Console.WriteLine("-2 Porcentagem equivalente a um valor");			

			int escolhaPorcen = int.Parse(Console.ReadLine());

			switch (escolhaPorcen)
			{
			     case 1:
			       Console.WriteLine("Digite um numero:");
			       double numero1 = double.Parse(Console.ReadLine());
			       Console.WriteLine("Qual porcentagem deseja descubrir do valor dado?");
			       double porcenValor = double.Parse(Console.ReadLine());

			       double Div100 = numero1 / 100;
			       double multiPorcen = Div100 * porcenValor;

			       Console.WriteLine(porcenValor + "% de " + numero1 + " é " + multiPorcen);
			     break;

			     case 2:
			       Console.WriteLine("Digite um numero:");
			       double numero2 = double.Parse(Console.ReadLine());
			       Console.WriteLine("Qual valor deseja descubrir a equivalencia em porcentagem?");
			       double dadoValor = double.Parse(Console.ReadLine());
          
			       double multiValor = dadoValor * 100;
			       double ResulPorcen = multiValor / numero2;
			       
			       Console.WriteLine(dadoValor + " equivale a " + ResulPorcen + "% de " + numero2);
			     break;

			     default:
              Console.WriteLine("Escolha uma opção valida!");
              Main();
            break;
			}
			Console.WriteLine();
			Main();
		}
		static void GeomPlana()
		{
			Console.WriteLine("Qual função deseja utilizar?");
			Console.WriteLine("   ");
			Console.WriteLine("-1 Area do Quadrado/Retangulo");
			Console.WriteLine("-2 Area do Triangulo");
			Console.WriteLine("-3 Altura do Triangulo");
			Console.WriteLine("-4 Area da circunferencia");
			Console.WriteLine("-5 Perimetro da Circunferêncua");
			Console.WriteLine("-6 Cateto de um Triangulo");			

			int escolhaFunc = int.Parse(Console.ReadLine());
		    switch (escolhaFunc)
		    {
		    	case 1:

		    	    Console.WriteLine("Digite o valor da Base");
		    	    double vlrBase = double.Parse(Console.ReadLine());
		    	    Console.WriteLine("Digite o valor da Altura");
		    	    double vlrAltura = double.Parse(Console.ReadLine());
		    	    
		    	    double vlrArea = vlrBase * vlrAltura;
		    	    
		    	    Console.WriteLine("A area da figura é " + vlrArea);
		    	    Console.WriteLine();		    	    
		    	    Main();
		    	break;
		    	   
		    	case 2:

		    	    Console.WriteLine("Digite o valor da base:");
		    	    double vlrBaseTri = double.Parse(Console.ReadLine());
		    	    Console.WriteLine("Digite o valor da altura:");
		    	    double vlrAlturaTri = double.Parse(Console.ReadLine());
           
		    	    double AreaTri = (vlrBaseTri * vlrAlturaTri) / 2;
           
		    	    Console.WriteLine("A area do tringulo é " + AreaTri);
		    	break;
		    	
		    	case 3:
		    	break;		    	

		    	case 4:
		    	break;

		    	case 5:
		    	break;		    	

		    	case 6:       
		    	break;
		    }
		}      
	}  
}
