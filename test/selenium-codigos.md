# Selenium - Códigos

## Códigos 

Alguns códigos do próprio **selenium**, implementado com o C\#, facilitando dentro de seus respectivos métodos

```csharp
public class SeleniumUtils
    {
        public readonly IWebDriver Browser;
        
        public void GoTo(string UrlParam)
        {
            Browser.Navigate().GoToUrl(Browser.Url + UrlParam);
        }
        public SeleniumUtils(IWebDriver webDriver)
        {
            this.Browser = webDriver ?? throw new System.ArgumentNullException(nameof(webDriver));
        }
        public IWebElement FindById(string Id)
        {
            return this.Browser.FindElement(By.Id(Id));
        }
        public IWebElement FindByClass(string name)
        {
            return this.Browser.FindElement(By.ClassName(name));
        }
        public IWebElement FindByName(string name)
        {
            return this.Browser.FindElement(By.Name(name));
        }
        public void WriteOnElement(IWebElement element, string text)
        {
            element.SendKeys(text);
        }
        public IWebElement GetByXPath(string xpath)
        {
            return this.Browser.FindElement(By.XPath(xpath));
        }
    }
```

