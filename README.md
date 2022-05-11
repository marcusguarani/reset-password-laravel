# reset-senha-laravel

[![issu Status](https://img.shields.io/github/issues/ok9xnirab/laravel-reset-password)](https://github.com/IANirab/laravel-reset-password/issues)
[![Build Status](https://travis-ci.org/boennemann/badges.svg?branch=master)](https://github.com/IANirab/laravel-reset-password/releases) ![folk Status](https://img.shields.io/github/forks/ok9xnirab/laravel-reset-password)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/IANirab/laravel-reset-password/issues)

This is a Laravel Package , where you can send 6-digits unique password in users. These Package Can easily validate users email if its listed or not !!

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
