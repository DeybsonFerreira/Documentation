# Functions

## Format with dinamyc mask

```csharp
//string cpf = "368924373";
//string mask = "00.000.000-0";

//cpf.FormatWithMask(cpf , mask )
//Output: 36.892.437-3


public static string FormatWithMask(this string input, string mask)
    {
        if (string.IsNullOrWhiteSpace(mask))
            return input;

        var output = string.Empty;
        var index = 0;

        foreach (var m in mask)
        {
            if (m == '0')
            {
                if (index < input.Length)
                {
                    output += input[index];
                    index++;
                }
            }
            else
                output += m;
        }

        return output;
    }
```

