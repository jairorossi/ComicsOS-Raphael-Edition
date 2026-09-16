# 🚀 ComicsOS 12.1 — Raphael Edition
### *By Jairo Rossi*
> **Android 12L / 12.1 (v1.0 Codename: Zero) para Xiaomi Mi 9T Pro / Redmi K20 Pro (aphael)**

---

## 📌 Sobre esta Build & Reconhecimentos

> [!NOTE]
> **Aviso de Uso Pessoal:** Esta é uma compilação de uso pessoal que estou disponibilizando abertamente para a comunidade e para qualquer entusiasta que queira testar e utilizar no Xiaomi Mi 9T Pro (aphael). O software é fornecido *"como está"* (as-is), fruto de muito trabalho e dedicação para entregar uma experiência fluida, estável e moderna.

### 🙏 Reconhecimentos e Créditos Especiais:
* **IronOS / IronLOS:** Base primordial utilizada para a construção e evolução deste projeto. Todo o respeito e créditos aos mantenedores da base Iron por fornecerem a fundação do sistema.
* **LineageOS & crDroid:** Pela infraestrutura open source, árvores de dispositivos e referências de drivers do Snapdragon 855 (sm8150).
* **Comunidade Raphael (Penglezos & Devs):** Pelos anos de suporte e desenvolvimento contínuo para manter o Mi 9T Pro vivo e atualizado.

---

## 📜 Changelog Completo & Correções Realizadas

### 1. 🎨 Nova Identidade Visual (ComicsOS - Zero Edition)
* **Rebranding Estrutural:** Migração de toda a árvore de vendor (endor/iron ➔ endor/comics).
* **Interface Personalizada:** Logotipo oficial da ComicsOS integrado na seção *Configurações > Sobre o Dispositivo*.
* **Menu Comics Custom:** Central de personalizações exclusivas com opções de estilo e customização de interface.
* **Wallpaper e Temas:** Wallpaper oficial temático do Batman e paleta de cores temática integrada com Monet.

### 2. 📸 Subsistema de Câmera & Lentes Auxiliares (GCam Ready)
* **Suporte Completo a Todas as Lentes Físicas:**
  * Sensor Principal Traseiro (Sony IMX586 - 48MP)
  * Câmera Frontal Motorizada Pop-up (Samsung S5K3T2 - 20MP)
  * Lente Teleobjetiva Física (OmniVision OV8856 - 8MP — ID 20)
  * Lente Ultra-Wide Física (Samsung S5K3L6 - 13MP — ID 21)
* **Whitelist CamX Restaurada:** endor.camera.aux.packagelist calibrada rigorosamente para os pacotes de câmeras do usuário (com.mi9series.camera, com.android.hasli.lmc82r9, com.android.camera, org.codeaurora.snapcam), eliminando de vez o erro Camera 100: Error configuring streams: Function not implemented (-38).
* **Framework Limpo:** Remoção de spoofing de pacotes instáveis no CameraManager.java para garantir estabilidade em multi-threading e conexões Camera2 API.

### 3. 🖥️ Stack Gráfica, EGL & Display HAL (SM8150)
* **Calibração de Cores e Display QTI:** Sincronização de 100% das propriedades endor.display.* e calibração QDCM com a árvore funcional de referência do Snapdragon 855.
* **Resolução do Erro EGL (GLContext / eglChooseConfig):** Remoção de propriedades conflitantes (debug.egl.hw=0, debug.sf.hw=0, skiavk) que forçavam emulação por software e causavam crash de EGL_NOT_INITIALIZED ao abrir o visor gráfico das GCams.
* **Aceleração Gráfica Nativa:** Renderização OpenGL ES 3.2 e Vulkan acelerada diretamente pela GPU Adreno 640.

### 4. 📐 Interface Dinâmica & Correção de DPI Customizado
* **Janelas de Diálogo do Sistema:** AppErrorDialog e BaseErrorDialog migrados para TYPE_APPLICATION_OVERLAY com largura MATCH_PARENT e centralização dinâmica.
* **Compatibilidade com DPIs Customizados:** Interface perfeitamente alinhada mesmo em densidades não-padrão (como 436dp), evitando caixas de diálogo cortadas ou desalinhadas.

### 5. 🛡️ Segurança, SELinux & Compilação
* **Build Userdebug Limpa:** Compilação otimizada eliminando violações de *neverallow* no SELinux.
* **Compatibilidade com Magisk / Root:** Desativação de spoofers de chaves internas agressivos para facilitar certificação Play Integrity e ocultação de root via Zygisk.
* **Limpeza de Pacotes:** Remoção de bloatwares e pacotes legados obsoletos (como QuickSearchBox AOSP).

---

## 📥 Downloads e Arquivos Necessários

### 📦 Links Permanentes no GitHub Releases:

| Arquivo | Descrição | Link de Download Direto |
| :--- | :--- | :--- |
| 🦊 **OrangeFox Recovery** | Recovery R12.0 Unofficial específico para Raphael | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/OrangeFox-R12.0-Unofficial-raphael-20260907.zip) |
| 📶 **Firmware MIUI 12.5.2** | Firmware Oficial MIUI Global Android 11 para Raphael | [Baixar no Gofile](https://gofile.io/d/iMakeCes) |
| 📱 **ROM ComicsOS Raphael** | ROM ComicsOS Zero Official (Android 12.1) | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/Comics-Zero-OFFICIAL-raphael-20260916.zip) |
| 🌐 **NikGapps ComicsOS** | Pacote GApps customizado e específico para a ComicsOS | [Baixar no GitHub](https://github.com/jairorossi/ComicsOS-Raphael-Edition/releases/download/v1.0-zero/NikGapps-ComicsOS.zip) |

---

## 📲 Guia de Instalação Passo a Passo (Clean Flash)

> [!IMPORTANT]
> A instalação de GApps imediatamente após a troca de ROM na mesma sessão de recuperação pode falhar devido a alterações no layout das partições dinâmicas. Seguir rigorosamente a sequência de reinicializações abaixo garante uma instalação 100% perfeita.

1. **Entrar no Recovery:**
   * Reinicie o aparelho no **OrangeFox Recovery** (OrangeFox-R12.0-Unofficial-raphael-20260907.zip).

2. **Formatar Dados (Format Data):**
   * Vá em **Wipe** > **Format Data** e digite yes.

3. **Wipe Avançado:**
   * Vá em **Advanced Wipe** e selecione:
     * Dalvik / ART Cache
     * Cache
     * System
     * Vendor
     * Metadata
     * Data
   * Arraste para confirmar a limpeza.

4. **Reiniciar no Recovery:**
   * Menu > **Reboot** > **Recovery**.

5. **Instalar o Firmware:**
   * Instale o pacote de **Firmware Android 11** (FW A11 / MIUI 12.5.2).

6. **Instalar a ROM:**
   * Instale o arquivo ZIP da **ComicsOS** (Comics-Zero-OFFICIAL-raphael-20260916.zip).

7. **Reiniciar no Recovery Novamente (Obrigatório):**
   * Menu > **Reboot** > **Recovery** *(necessário para carregar as novas partições antes dos GApps)*.

8. **Instalar os GApps:**
   * Instale o pacote **NikGapps-ComicsOS.zip** *(pacote exclusivo otimizado para esta ROM)*.

9. **Format Data Final:**
   * Faça novamente um **Format Data** (yes) para garantir que o armazenamento interno inicie limpo e sem conflitos de encriptação.

10. **Reiniciar no Sistema:**
    * Selecione **Reboot System** e aproveite a sua ComicsOS! 🚀
