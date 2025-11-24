# 🚀 Design Avançado: Annotation Personalizada e Metadata (Simulação ORM)

Este projeto demonstra a capacidade de criar e aplicar **metadata** (dados sobre dados) em código Java utilizando Annotations personalizadas. Ele simula a arquitetura fundamental de frameworks de ORM (Object-Relational Mapping), como o **JPA/Hibernate**, onde classes Java são mapeadas para recursos externos (tabelas de banco de dados).

---

## 🎯 Objetivo Principal

Criar uma Annotation (`@Tabela`) que receba um parâmetro (`nomeTabela`) e aplicar esta metadata a uma classe, provando que é possível ler essa informação em tempo de execução via Reflexão.

## 🛠️ Tecnologias e Conceitos de Design

* **Linguagem:** Java (Avançado)
* **Recursos:** Annotations, Meta-Annotations (`@Retention`, `@Target`).
* **Conceito Implícito:** **Reflexão (Reflection)** e **Mapeamento de Objetos (ORM)**.

## 🔑 Pontos de Destaque no Código

* **Metadados em Runtime:** Uso da meta-anotação `@Retention(RetentionPolicy.RUNTIME)` para garantir que a Annotation esteja disponível para leitura pela JVM após a compilação.
* **Escopo de Classe:** `@Target(ElementType.TYPE)` define que `@Tabela` só pode ser aplicada a classes ou interfaces, refletindo o uso em arquiteturas ORM.
* **Acoplamento Reduzido:** A anotação permite que a classe `TesteTabela` carregue informações sobre o seu recurso externo (o nome da tabela) sem precisar de código boilerplate ou herança complexa.
