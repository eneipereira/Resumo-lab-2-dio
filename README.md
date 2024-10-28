# Resumo-lab-2-dio

## Passo a Passo para criar uma AVM

### 1. Acessar o Portal da Azure

Vá até o portal da Azure e faça login com sua conta.


### 2. Navegar até "Máquinas Virtuais"

No menu à esquerda, clique em "Máquinas Virtuais" ou, se não aparecer, procure por "Máquinas Virtuais" na barra de pesquisa no topo.


### 3. Criar uma Nova Máquina Virtual

Na página de máquinas virtuais, clique no botão "Criar" e selecione "Máquina Virtual".


### 4. Configurar o Básico da VM

Agora você vai fornecer informações essenciais para configurar a máquina virtual:

Assinatura: Escolha a assinatura da Azure que você está utilizando (se houver mais de uma).

Grupo de Recursos: Escolha um grupo de recursos existente ou crie um novo. Um grupo de recursos organiza recursos relacionados da Azure.

Nome da VM: Defina um nome para sua máquina virtual (ex: "VM-Servidor").

Região: Escolha a localização geográfica onde a máquina será hospedada. Ex.: "East US". Escolha a região que está mais próxima de seus usuários para melhorar a latência.

Imagem: Escolha o sistema operacional da VM (Windows, Linux, etc.). Ex.: "Ubuntu Server 20.04 LTS".

Tamanho: Selecione o tamanho da VM, que define a quantidade de vCPUs, memória, e outras características. Ex.: B1s (básico e econômico) ou D2s_v3 (para mais desempenho).

Autenticação: Escolha como vai acessar a VM. Pode ser por:

Senha: Para logins usando nome de usuário e senha.

Chave SSH: Para acesso mais seguro no Linux.



### 5. Configurar o Disco (Armazenamento)

Escolha o tipo de disco do sistema operacional (OS disk):

Standard HDD: Disco rígido padrão (mais barato, menor desempenho).

Standard SSD: Disco sólido padrão (equilíbrio entre desempenho e custo).

Premium SSD: Disco sólido premium (maior desempenho).


Se necessário, adicione discos de dados para armazenamento adicional.


### 6. Configurar a Rede

Configure a rede virtual (ou use uma existente). Cada VM precisa estar associada a uma rede.

Configure uma sub-rede dentro dessa rede virtual.

Escolha se deseja um IP Público, para que a VM seja acessível externamente (por SSH ou RDP).

Defina as regras de firewall. Por padrão, as portas para RDP (porta 3389 para Windows) ou SSH (porta 22 para Linux) são abertas para permitir o acesso remoto.


### 7. Revisar as Outras Configurações (opcional)

Gerenciamento: Configure opções como monitoramento, backups, e automação.

Avançado: Para adicionar scripts personalizados, configurações de nuvem, e outras opções avançadas.

Tags: Adicione tags (marcadores) para organizar os recursos.


### 8. Revisar e Criar

Revise todas as configurações. Se estiverem corretas, clique em "Revisar + Criar".

O Azure fará uma validação das configurações e, se tudo estiver certo, você verá o botão "Criar".

Clique em "Criar" para iniciar a criação da VM.


### 9. Aguardar a Implantação

O processo de criação pode levar alguns minutos. Você verá o status da implantação e, quando estiver concluído, verá uma mensagem de sucesso.


### 10. Acessar a Máquina Virtual

Uma vez criada, vá até a VM recém-criada na página de máquinas virtuais.

Se configurou um IP público:

Para Linux: Acesse via SSH usando o IP público, por exemplo:

ssh usuario@IPVM

Para Windows: Abra o RDP no seu computador e insira o IP público da VM.
