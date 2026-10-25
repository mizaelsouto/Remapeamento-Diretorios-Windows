# 📁 Remapeamento e Migração de Diretórios de Usuários no Windows (`PowerShell`)

![PowerShell](https://img.shields.io/badge/PowerShell-5.1_%7C_7+-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-10_%7C_11-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-emerald?style=for-the-badge)

Suíte de scripts em **PowerShell** para **Windows 10 e Windows 11** projetada para redirecionar, restaurar e migrar automaticamente as pastas de perfil do usuário (*Documentos, Área de Trabalho, Downloads, Imagens, Vídeos e Músicas*) para uma unidade secundária (`D:`, `E:`, etc.), independentemente do idioma do sistema operacional.

Ideal para computadores com **SSDs pequenos (128 GB ou 250 GB)** na unidade `C:`, mantendo o sistema operacional leve e automatizando a gravação de arquivos na unidade de dados sem necessidade de mover pastas manualmente.

---

## 🛠️ Scripts Disponíveis e Documentação Detalhada

| Script PowerShell | Guia Específico | Função Principal |
| :--- | :--- | :--- |
| **`Redirect-UserFolders.ps1`** | [📖 Ler Guia de Redirecionamento](./README-Redirect-Folders.md) | Redireciona as pastas do usuário da unidade `C:` para outra unidade (`D:`, `E:`). Cria automaticamente Ponto de Restauração e backup do Registro. |
| **`Restore-UserFolders.ps1`** | [📖 Ler Guia de Restauração](./README-Restore-Folders.md) | Reverte o redirecionamento, restaurando os caminhos originais das pastas de usuário no Registro do Windows. |
| **`Copy-WindowsUsers.ps1`** | [📖 Ler Guia de Cópia/Migração](./README-Copy-Users.md) | Auxilia em cenários de formatação e manutenção, copiando de forma estruturada os dados de usuários de uma instalação antiga para uma nova. |

---

## 🚀 Boas Práticas de Execução

1. **Permissões de Administrador:** Execute sempre o PowerShell como **Administrador**.
2. **Localização do Script:** No caso do `Redirect-UserFolders.ps1`, execute-o a partir da raiz `C:\` ou de um pendrive (nunca de dentro de uma pasta que será movida, como *Desktop* ou *Downloads*).
3. **Ponto de Restauração:** Confirme a criação do Ponto de Restauração antes de prosseguir com alterações de Registro.

```powershell
# Exemplo de liberação temporária de execução na sessão atual do PowerShell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

# Executar o redirecionamento
.\Redirect-UserFolders.ps1
```

---

## ⚠️ Termo de Responsabilidade e Isenção de Danos

O uso destes scripts é de total e exclusiva responsabilidade do usuário:
- **Isenção de Garantia:** O desenvolvedor não fornece garantias quanto à compatibilidade absoluta com ambientes customizados.
- **Backup Prévio:** Recomenda-se fortemente possuir um **backup externo** dos seus dados importantes antes de executar qualquer script que altere o Registro ou mova diretórios de sistema.

---

## 📄 Licença & Autor

Distribuído sob a licença **MIT** ([LICENSE](./LICENSE)).  
Desenvolvido por **Mizael Souto** (`@mizaelsouto`) — [LinkedIn](https://www.linkedin.com/in/mizaelsouto)
