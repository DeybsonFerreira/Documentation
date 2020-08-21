---
description: Desenvolvimento à testes
---

# Test

## Selenium

      O **Selenium** é uma ferramenta usada para testes **automatizados**, interpretado pelo navegador, fazendo com que todo seu processo seja testado, trazendo uma garantia para seu produto.  
       Ele tem seus próprios códigos que são usados como por exemplo para :  
pegar algum elemento da tela, fazer o click, escrever em inputs, verificar componentes na tela e muitos outros.  
       **Interessante:** O selenium pode ser usado em **qualquer linguagem** Web  


```csharp
 public void SearchOnGoogle()
{
    IWebDriver Browser = new ChromeDriver();
    Browser.Url = "https://www.google.com/"; //irá abrir o google
    IWebElement input = base.Utils.FindByName("q");//irá encontrar o input do google
    input.SendKeys("irá escrever no input do google");//escrever
    IWebElement btnSearch = base.Utils.GetByXPath("//div[3]/center/input");
    btnSearch.Click();//clicar no botão para pesquisar
}
```

{% hint style="info" %}
Pacotes Usados para instalação do Selenium, podem ser instalados pelo NugetPackage ou Npm

\__Selenium WebDrive_r  
-WebDriver _ChromeDriver_ \( para suporte ao Chrome\)
{% endhint %}

