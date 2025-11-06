using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using static System.Console;
using System.IO;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            const string nomeArquivo = "TechFuture.csv";
            List<string> TechFuture;
            if (File.Exists(nomeArquivo))
            {
                TechFuture = new List<string>(File.ReadAllLines(nomeArquivo));
                WriteLine("Dados carregados com sucesso do arquivo 'TechFuture.csv'");
                WriteLine("Pressione qualquer tecla para iniicar...");
                ReadKey();
            }
            else
            {
                TechFuture = new List<string>();
            }
            bool sair = false;
            while (sair)
            {
                Clear();

                WriteLine("================================");
                WriteLine("     Gerenciador de Estoque     ");
                WriteLine("1. Inserir um novo produto");
                WriteLine("2. Procurar um produto");
                WriteLine("3. Total de produtos");
                WriteLine("4. Valor total de estoque");
                WriteLine("5. Listar todos os produtos");
                WriteLine("6. Salvar produtos em arquivo");
                WriteLine("7. Sair do programa");
                WriteLine("=================================");
                Write("Escolha uma opção:");

                string opcao = ReadLine();

                switch (opcao)
                {
                    case "1":
                        WriteLine("Digite o nome do produto para inserir (e o segmento):");
                        string nomeParaInserir = ReadLine();
                        TechFuture.Add(nomeParaInserir);
                        WriteLine($"'{nomeParaInserir}' foi adicionado com sucesso!");
                        break;
                    case "2":
                        Write("Digite o produto que deseja procuarar: ");
                        string nomeParaProcurar = ReadLine();
                        if (TechFuture.Contains(nomeParaProcurar))
                        {
                            WriteLine($"BOA NOTÍCIA: O produto '{nomeParaProcurar}' foi encontado na lista!");
                        }
                        else
                        {
                            WriteLine($"AVISO: O produto '{nomeParaProcurar}' NÃO foi encontrado.");
                        }
                        break;
                    case "3":
                        Write("Total de prdutos em estoque:");
                        string TotalProdutos = ReadLine();
                        if (TechFuture.Contains(TotalProdutos))
                        {
                            WriteLine($"O total de produtos: {TotalProdutos}");
                        }
                        else
                        {

                        }
                        break;
                    case "4":
                        Write("Valor total do estoque");
                        decimal totalEstoque = 0.0M;
                        foreach (var estoque in totalEstoque)
                        {
                            totalEstoque += estoque.Preco;
                        }
                        break;
                    case "5":
                        WriteLine("\n--- Lista de Produtos Cadastros ---");
                        if (TechFuture.Count == 0)
                        {
                            WriteLine("A lista esta vazia");
                        }
                        else
                        {
                            foreach (string nomeNaLista in TechFuture)
                            {
                                WriteLine($"- {nomeNaLista}");
                            }
                        }
                        WriteLine("----------------------------------------");
                        break;
                    case "6":
                        File.WriteAllLines(nomeArquivo, TechFuture);
                        WriteLine($"Lista de produto slava com sucesso no arquivo '{nomeArquivo}'!");
                        break;
                    case "7":
                        WriteLine("Encerrando o programa... Até logo!");
                        sair = true;
                        break;
                    default:
                        WriteLine("Opção inválida! Por favor, escolha um número de 1 a 7.");
                        break;

                }
                if (!sair)
                {
                    WriteLine("\nPressione qualquer tecla para continuar...");
                    ReadKey();
                }
            }
        }
    }
}
