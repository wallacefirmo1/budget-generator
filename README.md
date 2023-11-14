# budget-generator
Gerador de Orçamento feito em linguagem Python

## Modelo Impresso

Segue abaixo "output" do projeto.

![Gerador de Orçamento](https://docs.google.com/uc?id=1yimkqRkNumbe0zJ0SjCtby2oRvw8es0B) [1] 


## Gerador de Orçamento

### Mostrando dados para o usuário


```python
print("Orçamento gerado com sucesso!")
```

    Orçamento gerado com sucesso!


### Entrada de dados do usuário


```python
input("Digite o seu nome: ")
input("Digite o nomo do Projeto")
input("Digite a quantidade de horas prevista: ")
input("Digite o valor da hora trabalhado: ")
input("Digite o prazo estimado: ")
```

    Digite o seu nome: Wallace
    Digite o nomo do ProjetoDesenvolvimento Python
    Digite a quantidade de horas prevista: 200
    Digite o valor da hora trabalhado: 100
    Digite o prazo estimado: 3 meses





    '3 meses'



### Armazenado dados em variáveis

- nomes significativos (dicas)
- não


```python
projeto = "Semana do Python na Prática"
```


```python
print(projeto)
```

    Semana do Python na Prática



```python
projeto = input("Digite a descrição do projeto: ")
horas_previstas = int(input("Digite a quantidade de horas previstas: "))
valor_hora = int(input("Digite o valor da hora trabalhada: "))
prazo = input("Digite o prazo estimado: ")

```

    Digite a descrição do projeto: Desenvolvimento Python
    Digite a quantidade de horas previstas: 200
    Digite o valor da hora trabalhada: 150
    Digite o prazo estimado: 3 meses


### Realizando cáculos com o Python

- quantidade de horas prevista * valor horas trabalhada


```python
type(horas_previstas)
```




    int




```python
valor_total = horas_previstas * valor_hora
```


```python
print(valor_total)
```

    30000


### Gerando o PDF


```python
!pip install fpdf
```

    Collecting fpdf
      Downloading fpdf-1.7.2.tar.gz (39 kB)
      Preparing metadata (setup.py) ... [?25ldone
    [?25hBuilding wheels for collected packages: fpdf
      Building wheel for fpdf (setup.py) ... [?25ldone
    [?25h  Created wheel for fpdf: filename=fpdf-1.7.2-py2.py3-none-any.whl size=40705 sha256=6773b2a87642962c1943d636bd801acdee43e6da42202acd2a7f98c8b5374a05
      Stored in directory: /Users/wallacefirmo/Library/Caches/pip/wheels/44/35/8b/86ce00cec7e4d13c5f189680ae0fa82f919bedc066c2cddae9
    Successfully built fpdf
    Installing collected packages: fpdf
    Successfully installed fpdf-1.7.2



```python
from fpdf import FPDF
```


```python
pdf = FPDF()

pdf.add_page()
pdf.set_font("Arial")

pdf.image("template.png", x=0, y=0)

pdf.text(115, 145, projeto)
pdf.text(115, 160, str(horas_previstas))
pdf.text(115, 175, str(valor_hora))
pdf.text(115, 190, prazo)
pdf.text(115, 205, str(valor_total))

pdf.output("Orçamento.pdf")

print("Orçamento gerado com sucesso!")
```

    Orçamento gerado com sucesso!


# FRASE DO DIA 

## *Tudo é fácil com um bom direcionamento*

