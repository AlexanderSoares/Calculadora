# Calculadora

using System;

class Calculadora {
    static void Main(string[] args) {
        // Solicitar ao usuário que insira o primeiro número
        Console.Write("Digite o primeiro número: ");
        double num1 = Convert.ToDouble(Console.ReadLine());

        // Solicitar ao usuário que insira o segundo número
        Console.Write("Digite o segundo número: ");
        double num2 = Convert.ToDouble(Console.ReadLine());

        // Apresentar as opções de operações disponíveis
        Console.WriteLine("Escolha a operação:");
        Console.WriteLine("1 - Adição");
        Console.WriteLine("2 - Subtração");
        Console.WriteLine("3 - Multiplicação");
        Console.WriteLine("4 - Divisão");
        Console.Write("Digite o número da operação desejada: ");

        // Ler a escolha do usuário
        int escolha = Convert.ToInt32(Console.ReadLine());

        double resultado = 0;

        // Realizar a operação conforme a escolha do usuário
        switch (escolha) {
            case 1:
                resultado = num1 + num2;
                break;
            case 2:
                resultado = num1 - num2;
                break;
            case 3:
                resultado = num1 * num2;
                break;
            case 4:
                if (num2 != 0) {
                    resultado = num1 / num2;
                } else {
                    Console.WriteLine("Erro: divisão por zero.");
                    return;
                }
                break;
            default:
                Console.WriteLine("Opção inválida.");
                return;
        }

        // Exibir o resultado
        Console.WriteLine("O resultado da operação é: " + resultado);
    }
}
