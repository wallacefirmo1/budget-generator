# budget-generator
Gerador de Orçamento feito em linguagem Python

## Modelo Impresso

Segue abaixo "output" do projeto.

![Gerador de Orçamento](https://doc-10-c8-docs.googleusercontent.com/docs/securesc/mbd3jsqr0v7s5iu0ja6sifhc37nejvr8/vrqmit6or3utbg0ossiuf0gk3bn569nr/1699974150000/09626044948969061689/09626044948969061689/1yimkqRkNumbe0zJ0SjCtby2oRvw8es0B?ax=AI0foUoioLnKzGQ8fAe5vNnbyh8czS2q0jRhjlJYY6LSey98O6wnr0npKXVEvy0OzBWeONiHZlptjNjoqbmqsoesL7-o_nUJylPil06pHLODtMHMSMLLFQj-MtlY-EHWOhuHdzdYba5eKtzKytsyjmtHimPpEKBv3sphAJyhlpSxqSFfHCsHNx9TLP_SPHPGygQVa06SRSkx67YA29uRvsFqAHlhQo3-EOsT2uZA_VcnCAHvMdeYxd5EMqI6zyF1bT0sqwwEn9F29tS3_81rv_ym_Mh_SllLP4Sa8ZkKBEC63QW5gRfwxHyPI85WAGYLCmGw9h0pYv_1hrkbp6wEM7GyedHjQM_Q_n_C3kRwSm_7LzWNL53kvrc0X6-fRyPKEWjctLG0Ec9BR8Hyk6SLIZr_NGNSSKDBolKprBYawiAcO-Pisgyd2RIYbD8kQZ9_qmbVij00P4i5YDcnwrAtAhvBMdMy7TofUjTnTzQB4ee0p2fp_DMZ8bsISm3mC5i6PZMtt6UeUwd1hRC1Bntjphhardi4ti_GMznGkHrM-jgRBwYMnOzbt9-Tua_QMU99J2zjjIajivyWzjOhWNf_UWjJHyjdFgugHL-l0CjDLwM4e363v7CRLxep6Kswd0Izx5gqxn6bma1DzZ3pnf_rBHz-bk66IM-DXs7kP0eyXoBvS2KksYnDX0xsjsR2z2kEljCgte71JxchaVPrSQHbbSs2L06xEgtUGqiwxOMzJbdEQIELCFVtmEh6x1wnrI72CckTjtW_7cNb2Vl-JD5u68EyQB4r5M-OGTTb5sswWQJ7qn0pv7bKO_KuYadZZ8yJkympaL3LHJIng2vK1Vsli6bFQLnq58jCCRuu8YiIoe8DBpyvQCQNASNApMr5d68X_ts&uuid=a2ccc680-e62a-48f9-94cb-7783f2c4ff55&authuser=0&nonce=4mqn7t489153s&user=09626044948969061689&hash=rge6ujfv4c6fokjvtbd35cj09gnq1qkk) [1] 


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

