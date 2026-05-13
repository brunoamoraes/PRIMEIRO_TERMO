# 🖥️ Sistemas Operacionais: Fundamentos e Ecossistemas
> **Objetivo:** Compreender a arquitetura, gerenciamento de recursos e as diferenças entre os principais SOs do mercado.

---

## 1. 📂 O que é um Sistema Operacional?
O SO é a camada de software entre o hardware e o usuário. Suas funções principais são:
*   **Gerenciamento de Processos:** Escalonamento e execução de programas.
*   **Gerenciamento de Memória:** Alocação de RAM e memória virtual.
*   **Gerenciamento de Arquivos:** Organização em diretórios e permissões.
*   **Interface:** GUI (Gráfica) ou CLI (Linha de Comando).

---

## 2. 🪟 Microsoft Windows
Baseado originalmente no MS-DOS e evoluído para a arquitetura **NT (New Technology)**.

*   **Arquitetura:** Kernel Híbrido.
*   **Sistema de Arquivos:** NTFS (padrão atual) e FAT32/exFAT.
*   **Características:** 
    *   Foco em compatibilidade de hardware e uso doméstico/corporativo.
    *   Registro do Windows (base de dados centralizada de configurações).
    *   PowerShell e WSL (Windows Subsystem for Linux) para desenvolvedores.

---

## 3. 🐧 Linux (O Kernel e as Distribuições)
Um sistema **Open Source** baseado na filosofia Unix, criado por Linus Torvalds.

*   **Arquitetura:** Kernel Monolítico.
*   **Sistema de Arquivos:** Ext4, Btrfs, XFS.
*   **Distribuições (Distros):**
    *   *Debian/Ubuntu:* Foco em facilidade e servidores.
    *   *Fedora/Red Hat:* Foco corporativo e estabilidade.
    *   *Arch Linux:* Foco em personalização profunda.
*   **Diferencial:** Gerenciamento de pacotes (APT, YUM/DNF) e permissões de usuário (root).

---

## 4. 🍏 Apple iOS e macOS
Ecossistemas fechados baseados no kernel **XNU** (derivado do BSD/Unix).

### macOS
*   Sistema para desktops e laptops.
*   Conhecido pela estabilidade e integração com hardware próprio (chips M1/M2/M3).

### iOS
*   Sistema móvel para iPhone.
*   **Segurança:** Arquitetura de "Sandboxing" (cada app isolado).
*   **Otimização:** Gerenciamento agressivo de memória e energia.

---

## 5. 🌐 Outros Sistemas Relevantes
*   **Android:** Baseado no kernel Linux, mas com uma stack de usuário (Java/Kotlin) diferente.
*   **RTOS (Real-Time OS):** Sistemas para fins específicos (como satélites ou carros) onde o tempo de resposta é crítico.
*   **Unix (Legado/Proprietário):** Solaris, AIX, HP-UX.

---

## 📊 Tabela Comparativa


| Recurso | Windows | Linux | macOS / iOS |
| :--- | :--- | :--- | :--- |
| **Núcleo (Kernel)** | Híbrido | Monolítico | XNU (Híbrido) |
| **Código** | Fechado | Aberto | Fechado |
| **Customização** | Média | Alta | Baixa |
| **Uso Principal** | Desktop/Games | Servidores/Nuvem | Design/Mobile |

---

## 🛠️ Atividade Prática
1.  **Linha de Comando:** Comparar os comandos `dir` (Windows) vs `ls` (Linux/Mac).
2.  **Monitoramento:** Abrir o *Gerenciador de Tarefas* (Win) e o comando `top` ou `htop` (Linux) para analisar o consumo de RAM.
