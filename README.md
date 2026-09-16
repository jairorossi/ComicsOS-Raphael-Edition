# 🚀 ComicsOS 12.1 - Raphael Edition (by Jairo Rossi)
> Versão oficial, customizada e otimizada da **ComicsOS (Android 12L / 12.1)** para **Xiaomi Mi 9T Pro / Redmi K20 Pro (`raphael`)**.

---

## ✨ Recursos e Destaques desta Edição (Changelog)

1. 🎨 **Identidade Visual Completa ComicsOS:**
   * Logotipo oficial integrado na tela de *Configurações > Sobre o Dispositivo*.
   * Menu exclusivo de customizações traduzido (*Comics Custom*).
   * Wallpaper padrão temático do Batman.
   * Versão oficial definida como **`ComicsOS Zero`**.

2. 📱 **Correção Dinâmica de Interface (DPI Customizado):**
   * Janela de erro do sistema (`AppErrorDialog`) migrada para `TYPE_APPLICATION_OVERLAY` com `MATCH_PARENT`.
   * Alinhamento centralizado perfeito mesmo com DPIs customizados (como 436dp), sem transbordar para fora da tela.

3. 📸 **Arquitetura de Câmera AOSP Pura:**
   * Framework Camera2 limpo e nativo, compatível com GCam (LMC, BSG, AGC, Shamim), ports MiuiCamera e qualquer app da Play Store sem restrições de pacotes.

4. 🌐 **Correção de Painéis de Sistema:**
   * Correção no Internet QS Tile para evitar tiles em branco no primeiro boot.
   * Otimização de layouts biométricos e de sistema.

---

## 📥 Guia de Instalação e Downloads

### 📦 Links Diretos dos Arquivos (GitHub Releases - Permanentes):

| Arquivo | Descrição | Link para Download Direto |
| :--- | :--- | :--- |
| 🦊 **OrangeFox Recovery** | Recovery R12.0 Unofficial específico para Raphael | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/OrangeFox-R12.0-Unofficial-raphael-20260907.zip) |
| 📶 **Firmware MIUI 12.5.2** | Firmware Oficial MIUI Global Android 11 para Raphael | [Baixar no Gofile](https://gofile.io/d/iMakeCes) |
| 📱 **ROM ComicsOS Raphael** | ROM ComicsOS Zero Official (Android 12.1) | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/Comics-Zero-OFFICIAL-raphael-20260916.zip) |
| 🌐 **NikGapps ComicsOS** | Pacote GApps customizado e otimizado para a ComicsOS | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/NikGapps-ComicsOS.zip) |

---

### 📲 Passo a Passo de Instalação Limpa (Clean Flash):

> [!IMPORTANT]
> A instalação do GApps imediatamente após a troca de ROM na mesma sessão de recuperação pode falhar devido a alterações no layout das partições. A ordem rigorosa abaixo garante uma instalação 100% limpa e sem erros.

1. **Entrar no Recovery:**
   * Reinicie no **OrangeFox Recovery** (`OrangeFox-R12.0-Unofficial-raphael-20260907.zip`).

2. **Formatar Dados (Format Data):**
   * Vá em **Wipe** > **Format Data** e digite `yes`.

3. **Wipe Avançado:**
   * Vá em **Advanced Wipe** e selecione:
     - `Dalvik / ART Cache`
     - `Cache`
     - `System`
     - `Vendor`
     - `Metadata`
     - `Data`
   * Arraste para confirmar o Wipe.

4. **Reiniciar no Recovery:**
   * Menu > **Reboot** > **Recovery**.

5. **Instalar Firmware:**
   * Instale o **Firmware Android 11** (`FW A11 / MIUI 12.5.2`).

6. **Instalar a ROM:**
   * Instale o pacote da **ComicsOS** (`Comics-Zero-OFFICIAL-raphael-20260916.zip`).

7. **Reiniciar no Recovery Novamente:**
   * Menu > **Reboot** > **Recovery** *(obrigatório antes de passar os GApps)*.

8. **Instalar os GApps:**
   * Instale o pacote **NikGapps-ComicsOS.zip** *(pacote otimizado especificamente para a ComicsOS)*.

9. **Format Data Final:**
   * Faça novamente um **Format Data** (`yes`) para garantir que a partição de dados inicie limpa e sem conflitos de encriptação.

10. **Reiniciar no Sistema:**
    * Selecione **Reboot System** e aproveite a ComicsOS! 🚀
