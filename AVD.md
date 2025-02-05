![image](https://github.com/user-attachments/assets/3ef1ad1d-9be7-4808-b9c5-77388a692678)# Arquitetura do AVD  

## 🔹 Visão Geral  
Este repositório documenta a arquitetura do Azure Virtual Desktop (AVD) de referência utilizada para garantir escalabilidade e segurança.  

## 📌 Componentes Principais  
- **Session Hosts:** Máquinas virtuais rodando Windows multi-session.  
- **FSLogix:** Gerenciamento de perfis de usuários.  
- **Azure Firewall:** Controle de tráfego entre redes.  
- **Entra ID:** Autenticação e controle de acesso.
- **Active Directory Domain Services**  Autenticação e controle de acesso.
- **Nat Gateway** Saída do tráfego de internet, integrao ao Azure Firewall.
- **VPN Gateway** Acesso remoto seguro aos servidores e session hosts do AVD.
- **Azure Bastion** Acesso remoto seguro aos servidores e session hosts do AVD como contigência em caso de falha da VPN.
- **Private DNS Zone** Configuração dos endereços privados para os storage accounts e Recovery Service Vault (backup).
- **Shared Gallery** Armazenamento das imagens Golden Image AVD.
- **Business Continuity Center (Backup)** Backup dos perfis de FSLogix.
- **Update Manager** Atualizações dos sistemas operacionais.
- **Defender for Endpoint** - Proteção para os servidores e session hosts

## 📊 Diagrama da Arquitetura  
![Desenho de Arquitetura AVD drawio](https://github.com/user-attachments/assets/3778e131-970b-4b39-975f-e52e6a53a52b)


## 🚀 Melhorias Futuras  
- Implementação de redundância em múltiplas regiões (DR).  


