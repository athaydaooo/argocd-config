# ArgoCD Config

Este repositório contém as configurações do ArgoCD para gerenciamento das aplicações dentro do cluster Kubernetes.

## Estrutura do Repositório

Cada aplicação do sistema ArgoCD possui sua própria pasta dentro deste repositório. Aplicações externas e demais serviços possuem seus manifestos de configuração nos respectivos repositórios.

```
/metallb/           # Configuração do MetalLB gerenciada pelo ArgoCD
/app1/              # Configuração da aplicação 1
/app2/              # Configuração da aplicação 2
...
```

## Configuração

A configuração inicial dos apps de sistema são gerenciadas pelo Helm, enquanto as demais atualizações e ajustes são realizados diretamente neste repositório.

## Sincronização com o ArgoCD

As aplicações definidas aqui são sincronizadas automaticamente pelo ArgoCD, garantindo que o estado desejado seja mantido no cluster.

## Como Aplicar Alterações

1. Faça um fork ou clone deste repositório.
2. Edite os manifestos YAML conforme necessário.
3. Faça commit e push das alterações.
4. O ArgoCD identificará automaticamente as mudanças e aplicará ao cluster.

## Contribuições

Se precisar adicionar ou modificar configurações, siga as práticas recomendadas do Kubernetes e garanta que os manifestos estejam corretamente validados antes do commit.

## Licença

Este projeto segue a licença [MIT](LICENSE).
