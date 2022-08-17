# Erro fatal: Authentication failed for [url-git] no Windows
Durante uma troca de clientes que eu estava trabalhando, não consegui fazer o clone do projeto de forma nenhuma.
No final da história descobri que o erro estava relacionado ao credential manager do GIT no Windows. 
Utilizei dois comandos:

1 - Verificar qual o tipo de credencial o sistema operacional estava usando:
```
git config --system credential.helper
```

2 - Dar um reset no tipo de credencial, para que o Windows volte a pedir o login e senha do GIT antes de baixar

```
git config --system --unset credential.helper
```
