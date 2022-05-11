# reset-senha-laravel


Este é um Pacote Laravel, onde você pode enviar uma senha exclusiva de 6 dígitos nos usuários. Esses pacotes podem validar facilmente o e-mail dos usuários, se estiver listado ou não !!

# Insatalação

`compositor requer nirab/reset-password`

adicione esta linha no array 'providers' de `config/app.php`

`nirab\resetpassword\ResetPasswordServiceProvider::class,`

então ,
use estes comandos para publicar o arquivo de configuração do pacote (resetpassword.php) na pasta de configuração e o modelo de e-mail na pasta views .

`fornecedor de artesão php:publicar`

abra o arquivo `.env` em seu projeto e também configure o banco de dados e a conexão de e-mail em primeiro lugar

# Uso

adicione essas linhas no topo do seu controlador

`use nirab\resetpassword\Models\UserResetPassword;`

Então,

<código>
$resetpassword = new UserResetPassword();

echo $resetpassword->SendMail($email);</code>

Observação :

\$email = Email de seus usuários.

# Customização

vá para `config/resetpassword.php`.
então você vê,

```bash
<?php
return [
    'msgSuccess' => 'A New Password Has Been Send to your Email !!',
    'msgError' => 'Email is not registered !!',
    'address' => 'mygmail@gmail.com',
    'name' => 'Reset Your Password :: site.com'
];
```
