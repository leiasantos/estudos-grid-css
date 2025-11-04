<h1>CSS Grid</h1>
<h2> 🧱 CSS Grid - Guia </h2>
<p>
  O **CSS Grid Layout** é um sistema bidimensional (linhas e colunas) que permite criar layouts complexos de forma simples e organizada.  
Com ele, é possível alinhar, distribuir e dimensionar elementos facilmente.
</p>

<h2>⚙️ Como ativar o Grid</h2>

<pre>
  <code>
.container {
  display: grid;
}
  </code>
</pre>

<p>Isso transforma o elemento .container em um Grid Container, e seus filhos viram Grid Items.</p>


## 🧱 Propriedades do CSS Grid

| 🧩 Propriedade | 📝 Descrição | 💻 Exemplo |  Resultado / Observação |
|----------------|--------------|-------------|----------------------------|
| **grid-template-columns** | Define o número e o tamanho das **colunas**. | ```css grid-template-columns: 200px 1fr 2fr;``` | 1ª: 200px<br>2ª: ocupa o espaço restante (1fr)<br>3ª: ocupa o dobro (2fr) |
| 💡 Exemplo prático | Cria 3 colunas iguais. | ```css grid-template-columns: repeat(3, 1fr);``` | 3 colunas de tamanhos iguais |
| **grid-template-rows** | Define o número e o tamanho das **linhas**. | ```css grid-template-rows: 100px auto 50px;``` | 3 linhas com tamanhos diferentes |
| **gap** | Controla o espaçamento entre as linhas e colunas. | ```css gap: 1rem;```<br>```css row-gap: 1rem;```<br>```css column-gap: 2rem;``` | Define espaçamento uniforme ou separado entre linhas e colunas |
| **justify-content** e **align-content** | Controlam **todo o conteúdo** dentro do grid. | ```css justify-content: center;```<br>```css align-content: center;``` | `justify-content` → eixo horizontal<br>`align-content` → eixo vertical |
| **justify-items** e **align-items** | Controlam o **alinhamento dos itens** dentro das células. | ```css justify-items: center;```<br>```css align-items: center;``` | `justify-items` → alinha horizontalmente<br>`align-items` → alinha verticalmente |
| **grid-column** e **grid-row** | Definem onde o item começa e termina. | ```css .item1 { grid-column: 1 / 3; grid-row: 1 / 2; }``` | O item ocupa da coluna 1 até a 3 e a linha 1 |
| **justify-self** e **align-self** | Alinham **individualmente** um item dentro da célula. | ```css .item1 { justify-self: end; align-self: start; }``` | Alinhamento individual dentro da célula |

---

📘 **Dica:** Combine `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));` para criar layouts **responsivos** que se ajustam automaticamente ao tamanho da tela.


## 📏 Unidades úteis do CSS Grid

| 🧮 Unidade | 📝 O que faz |
|-------------|--------------|
| **fr** | Fração do espaço disponível |
| **auto** | Tamanho automático conforme o conteúdo |
| **%** | Porcentagem em relação ao elemento pai |
| **min-content** | Menor tamanho possível que acomoda o conteúdo |
| **max-content** | Maior tamanho necessário para exibir todo o conteúdo |
| **minmax(min, max)** | Define um tamanho mínimo e máximo para a célula |

---

💡 **Exemplo prático:**
```css
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
