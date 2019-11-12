# Conceitos

## Orientação a Objeto

A orientação a objetos é uma ponte entre o mundo real e virtual, a partir desta é possível transcrever a forma como enxergamos os elementos do mundo real em código fonte, a fim de nos possibilitar a construção de sistemas complexos baseados em objetos.

**Exemplo**: para uma \( Pessoa \)

 **O que é uma pessoa?**

 A pessoa é um ser do mundo real que interage com toda a natureza.  
`class Pessoa    {     }`

· **Quais são as características de uma pessoa?**

Resposta: Uma pessoa possui: nome, olhos, boca, braços, pernas, cabelos e etc.  
`class Pessoa {  
 string nome;  
 int olhos,bracos,pernas;  
 string cor_olhos;  
 string cor_cabelos;  
             }`

· **Como uma pessoa se comporta?**

Resposta: Uma pessoa corre, anda, fala, pula, come e etc.  
`class Pessoa {  
      void Correr();  
      void Andar();  
      void Pular();     
             }`

## TimeStamp 🕐

{% tabs %}
{% tab title="TimeStamp" %}
 Representa um ponto específico na linha do tempo e leva em consideração o fuso horário em questão \(`UTC`\).  

E um número que determina um momento específico

ex: 

`1572535830` = que é equivalente a 31/10/2019 :15:30:30 no Brasil
{% endtab %}

{% tab title="DateTime" %}
Data original representada no calendário/relógio

ex: 31/10/2019: 15:30:30
{% endtab %}
{% endtabs %}



