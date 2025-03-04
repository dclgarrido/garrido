Este repositório documenta a arquitetura de referência utilizada para garantir a continuidade de negócios e a recuperação de desastres (DR) no Azure Virtual Desktop (AVD) em um ambiente híbrido. 
A solução é projetada para fornecer alta disponibilidade, segurança e resiliência operacional.

📌 Componentes Principais
Session Hosts: Máquinas virtuais rodando Windows multi-session distribuídas entre regiões primária e secundária.
FSLogix com Cloud Cache: Gerenciamento de perfis de usuários com redundância entre múltiplos Storage Accounts em diferentes regiões.
Azure Backup: Proteção de dados e recuperação de arquivos essenciais, incluindo perfis FSLogix e aplicações empresariais.
Appliances Firewall comm HA: Controle de tráfego entre redes para comunicação segura entre hubs e spokes das diferentes regiões.
Microsoft Entra ID: Autenticação e controle de acesso, integrado ao Active Directory local via Entra Connect.
Active Directory Domain Services: Sincronização e autenticação híbrida com DCs hospedados no Azure.
NVA: Conectividade híbrida entre o ambiente on-premises e o Azure.
Azure Bastion: Acesso remoto seguro para administração dos servidores e session hosts sem expor portas RDP/SSH.
Private DNS Zone: Resolução de nomes privados para os Storage Accounts e Backups com o Business Continuity Center.
Shared Image Gallery: Armazenamento centralizado de Golden Images para rápida recuperação e provisionamento de novos session hosts.
Update Manager e Intune: Gerenciamento de atualizações para manter a segurança e a conformidade do ambiente.
Defender for Endpoint: Proteção avançada contra ameaças para os session hosts e servidores.

![Arquitetura_Cloudcache drawio](https://github.com/user-attachments/assets/241d7e11-cb9d-4a68-a338-4df1331176f1)
