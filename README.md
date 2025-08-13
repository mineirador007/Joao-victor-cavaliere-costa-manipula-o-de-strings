
frases_para_lista.txt futebol tequila bola futebol torcida bola golero

dna.txt AATCTGCAC

texto.txt tesxto para teste do programa


inverso_dna.py
def ler_arquivo_dna(nome_arquivo):
        with open(nome_arquivo, 'r') as arquivo:
            cadeia_dna = arquivo.readline().strip()
            return cadeia_dna
def gerar_cadeia_inversa(cadeia_dna):
    validos = set('ATCG')
    cadeia_inversa = cadeia_dna[::-1]
    return cadeia_inversa
def main():
    nome_arquivo = 'dna.txt'
    cadeia_dna = ler_arquivo_dna(nome_arquivo)
    if cadeia_dna:
        cadeia_inversa = gerar_cadeia_inversa(cadeia_dna)
        if cadeia_inversa:
            print(f"Cadeia de DNA lida: {cadeia_dna}")
            print(f"Cadeia inversa: {cadeia_inversa}")
if __name__ == "__main__":
    main()


    
    
    
    
palavras_qtd.py
    def contar_palavras(nome_arquivo):
        with open(nome_arquivo, 'r', encoding='utf-8') as arquivo:
            texto = arquivo.read()
            palavras = texto.split()
            return len(palavras)
def main():
    numero_palavras = contar_palavras('texto.txt')
    print(f"O arquivo contém {numero_palavras} palavras.")
if __name__ == "__main__":
    main()






lista.py
def extrair_palavras_unicas(nome_arquivo):
    with open(nome_arquivo, 'r', encoding='utf-8') as arquivo:
        texto = arquivo.read()
        palavras = texto.split()
        palavras_unicas = list(dict.fromkeys(palavras))
        return palavras_unicas

def main():
    nome_arquivo = 'frases_para_lista.txt'
    palavras_unicas = extrair_palavras_unicas(nome_arquivo)
    print("Palavras unicas encontradas no arquivo:")
    print(palavras_unicas)
if __name__ == "__main__":
    main()








sem_espaços.py
def substituir_espacos(nome_arquivo):
        with open(nome_arquivo, 'r', encoding='utf-8') as arquivo:
            texto = arquivo.read()
            texto_modificado = texto.replace(' ', '_')
            return texto_modificado
def main():
    nome_arquivo = 'texto.txt'
    resultado = substituir_espacos(nome_arquivo)
    if resultado is not None:
        print("Texto com espaços substituídos por underlines:")
        print(resultado)
if __name__ == "__main__":
    main()
