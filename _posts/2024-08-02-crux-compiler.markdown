---
layout: post
title: "Compiler for a C-like Language (Project)"
categories: project
---

## About:

A compiler for Crux, a simplified C-like language which contains bool and int types, variables,  functions, control flow blocks (e.g. IF, FOR), and basic comparison (e.g. >, &&) and mathematical (e.g.+, /) operations. It recieves a file written in Crux and converts it to a x86-64 assembly listing, which can then be converted into an executable using GCC.

The compiler converts the initial code into many different forms before it is translated into assembly. First, the code is split into tokens and converted into a parse tree. Next, the parse tree is converted into an [Abstract Syntax Tree](https://en.wikipedia.org/wiki/Abstract_syntax_tree), where type checking is done. Next, is is converted into an [Intermediate Representation](https://en.wikipedia.org/wiki/Intermediate_representation), in this case being a graph with nodes as basic blocks and edges representing control flow. Finally, the graph is converted into assembly, with starts of blocks being given labels for jump commands.

This was made for ICS 142A with alongside one partner.

## Languages, Frameworks, Tools

- Java
- Maven
- ANTLR (Parser Generator)
- Github