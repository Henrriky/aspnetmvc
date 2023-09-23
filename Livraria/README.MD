# Comandos

- Ctrl + F5 -> Executar projeto
- Url tem um mapeamento automatico com o arquivo criado no controller.
- Estrutura
    - Nome do controller/actionName/parametros
    - É definido em `Program.cs`
    ```c#
        app.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
    ```

## Parametros de url

- Define-se parâmetros para nossos métodos: 
    ```c#
    public string Welcome (string name, int id = 1) {

        return HtmlEncoder.Default.Encode($"Oi {$name}, ID: ${id}");
    }
    ```
    - Url: 