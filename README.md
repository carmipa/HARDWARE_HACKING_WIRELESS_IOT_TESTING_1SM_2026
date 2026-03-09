# 🌐 Hardware Hacking & Wireless IoT Testing (1SM 2026)

<div align="center">

![Status](https://img.shields.io/badge/Status-Em%20Andamento-success?style=for-the-badge&logo=github)
![FIAP](https://img.shields.io/badge/FIAP-2026-ed145b?style=for-the-badge)
![Professor](https://img.shields.io/badge/Prof.-Marcelo%20Morgantini-blue?style=for-the-badge&logo=google-scholar)
![IoT](https://img.shields.io/badge/Tecnologia-IoT-00979D?style=for-the-badge&logo=iot)
![Eletrônica](https://img.shields.io/badge/Eletrônica-Básica-F34F1C?style=for-the-badge&logo=arduino)

</div>

> *"A Internet das Coisas não pode ser mais cara do que as próprias Coisas!"*

Este repositório consolida o conteúdo da disciplina **Hardware Hacking, Wireless e IoT Testing**, reunindo fundamentos técnicos sobre energia, eletrônica básica, protocolos de comunicação (como MQTT) e o vasto ecossistema da Internet das Coisas (IoT). 

---

## 📋 Sumário

- [Visão Geral](#-visão-geral)
- [Módulo 1: Conceitos de IoT](#-módulo-1-conceitos-de-iot)
- [Módulo 2: Fundamentos de Energia e Eletrônica](#-módulo-2-fundamentos-de-energia-e-eletrônica)
- [Arquitetura IoT (Diagrama)](#-arquitetura-iot-diagrama)
- [Professor e DNA FIAP](#-professor-e-dna-fiap)

---

## 📖 Visão Geral

A disciplina capacita o desenvolvimento de projetos de hardware e software, trabalhando os desafios da internet das coisas, desde o planejamento elétrico até a execução na nuvem. A tecnologia de IoT não se resume apenas a "acender lâmpadas pelo smartphone"; o objetivo é desenhar objetos inteligentes capazes de coletar dados do ambiente, analisá-los e tomar decisões autônomas.

### 🎯 Objetivos de Aprendizado:
- 🔌 **Eletrônica Básica** e Medição
- 🧠 **Microcontroladores** e Sensores 
- 🌩️ **Integração Cloud** e Automação
- 📡 **Protocolos** e Sistemas de Transporte TCP/IP

---

## 📡 Módulo 1: Conceitos de IoT

Baseado no material de introdução à IoT, a democratização e o barateamento da tecnologia tornaram o ecossistema acessível para integrações mundiais. 

### Evolução Histórica ⏱️
- **RFID** (Radio Frequency Identification)
- **WSN** (Wireless Sensor Network)
- **Internet padrão** (TCP/IP)
- **Redes Móveis:** 2G, 3G, 4G e 5G

### Principais Aplicações 🚀
* 🏠 **Automação Residencial e Comercial**
* 🌍 **Sensoriamento Ambiental**
* 🚗 **Redes Veiculares e Cidades Inteligentes**

As topologias frequentemente adotam o padrão **Cliente-Servidor**, funcionando por meio de softwares clientes que fazem requisições para controle. O foco se mantém em construir sistemas confiáveis em ambientes hostis de difícil acesso.

---

## ⚡ Módulo 2: Fundamentos de Energia e Eletrônica

A **energia** atua como motor de toda nossa tecnologia. Ela se manifesta de formas muito variadas, como eventos **Magnéticos, Térmicos, Químicos e Luminosos**. Como postulado nas aulas: *"A energia nunca desaparece, apenas se transforma"*.

### Eixos do Conhecimento Essencial:
1. **Matéria e Átomos ⚛️:** Compreensão da estrutura que nos cerca. Formação de prótons, elétrons e íons resultantes do desequilíbrio atômico.
2. **Condução Elétrica 🛤️:** A distinção física entre os materiais Condutores e os Isolantes.
3. **Leis de Ohm 📐:** A clássica 1ª Lei de Ohm e a definição de Corrente Elétrica.
4. **Comportamento de Circuitos 💡:** O relacionamento indispensável entre a corrente, tensão e resistência nos sistemas hardware que compõem os nós de IoT.

---

## 🏗 Arquitetura IoT (Diagrama)

Abaixo, um diagrama arquitetural padrão representando a troca de mensagens explicada nos fundamentos do curso, focando na integração via **Broker MQTT**:

```mermaid
graph TD;
    %% Definição de Cores Otimizadas para Modo Dark/Light
    classDef device fill:#2b2b2b,stroke:#00979D,stroke-width:2px,color:#fff;
    classDef broker fill:#005c8a,stroke:#00aaff,stroke-width:2px,color:#fff;
    classDef app fill:#e67300,stroke:#ff9500,stroke-width:2px,color:#fff;

    subgraph Dispositivos Físicos 🖲️
      A[Microcontrolador / Sensor]:::device -->|Lê Grandezas Físicas| B(Dados do Ambiente):::device
      C[Módulos de Atuação]:::device -->|Executa Ação| D(Relés / Motores):::device
    end

    subgraph Infraestrutura / Comunicação 🌐
      A -->|Publica Dados MQTT| E((Broker MQTT / Servidor)):::broker
      E -->|Envia Comandos MQTT| C
    end

    subgraph Aplicações Clientes 💻
      E -.->|Assina Tópico| F[App Mobile]:::app
      E -.->|Dashboard AWS/Cloud| G[Sistema Web]:::app
      F -.->|Envia Ação| E
    end
```

*(Conceito lógico desenhado conforme a infraestrutura de comunicação em nuvem analisada na disciplina)*

---

## 🎓 Professor e DNA FIAP

* 👨‍🏫 **Marcelo Fernando Morgantini (Morgs):** [prof.morgantini@fiap.com.br](mailto:prof.morgantini@fiap.com.br)
* 🎓 **Formação:** Graduado em Redes de Computadores / MBA em Gestão Corporativa de TI.
* 💼 **Atuação:** Tribunal de Justiça de São Paulo / Professor FIAP especializado em Cyber Security, Cloud Computing e Engenharia Mecatrônica.

---
<p align="center">
  <sub>Este material é formatado com base nos conteúdos oficiais (Aulas S1-A1 e S1-A2) ministrados na FIAP para a classe estudantil.</sub><br>
  <sub><i>Criado para facilitar estudos e colaborações de código no ecosistema da disciplina.</i></sub>
</p>