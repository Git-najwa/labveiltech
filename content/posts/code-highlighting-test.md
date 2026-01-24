---
title: "Les formats visuels et leurs usages"
date: 2026-01-12T10:00:00+08:00
draft: false
description: "Analyse des formats visuels et de leur pertinence selon le contexte de communication"
tags: ["formats", "communication visuelle", "stratégie"]
categories: ["Ressources"]
slug: code-highlighting-test
---

### Présentation de la ressource

La ressource analysée est un article publié par Riverside, intitulé *"What is Visual Communication & How to Best Use It?"*.

Il propose une définition structurée de la communication visuelle et présente les principaux formats utilisés pour transmettre un message : images, vidéos, graphiques, schémas ou animations. L'article adopte une approche pédagogique, en expliquant non seulement ce qu'est la communication visuelle, mais aussi dans quels contextes chaque format est le plus pertinent.

➜ [**Voir la ressource**](https://riverside.com/blog/what-is-visual-communication)

---

### Contexte et intérêt du contenu

En revenant sur les bases de la communication visuelle, l'article permet de mieux comprendre comment les messages prennent forme à travers différents supports. Il met en relation les objectifs de communication et les choix de formats, montrant que chaque support visuel répond à des usages spécifiques selon le contexte et le public visé.

Cette approche éclaire les mécanismes à l'œuvre dans la production et la diffusion de contenus visuels, en particulier dans les environnements numériques actuels.

---

### Apports et enjeux

L'article met en évidence plusieurs aspects clés de la communication visuelle :

- la communication visuelle comme moyen de transmettre une information de manière rapide et efficace ;
- la diversité des formats visuels, chacun répondant à des usages spécifiques (expliquer, synthétiser, illustrer, capter l'attention) ;
- l'adaptation des formats selon le contexte : par exemple, la vidéo pour engager, les graphiques pour clarifier des données, ou les images pour renforcer un message ;
- l'impact des visuels sur la compréhension et la mémorisation, en particulier dans des environnements saturés d'informations.

Ces éléments montrent que le choix d'un format visuel relève d'une décision stratégique, et non uniquement esthétique.

---

### Pistes d'exploitation

Cette ressource peut être utilisée comme référence de base pour analyser ou concevoir des messages visuels de manière plus réfléchie. Elle permet d'évaluer la pertinence d'un format en fonction de son objectif et de son contexte de diffusion.

Les principes présentés peuvent être transposés à différents projets de communication visuelle : analyse de contenus sur les réseaux sociaux, conception de supports graphiques ou audiovisuels, ou encore réflexion sur la forme la plus adaptée pour transmettre une information.

L'article fournit ainsi un cadre utile pour penser la communication visuelle au-delà d'un simple choix esthétique, en lien direct avec l'intention du message.

        for item in self.data:
            if self.validate_item(item):
                result['processed'].append(item)

        return result
```

## Highlighting Specific Lines

```go {lineNos=true hl_lines=[3,6,8]}
package main

import "fmt"  // This line will be highlighted

func main() {
    message := "Hello, World!"  // This line will also be highlighted

    fmt.Println(message)  // This line will also be highlighted

    for i := 0; i < 3; i++ {
        fmt.Printf("Count: %d\n", i)
    }
}
```


## Codeblock with Filename

```typescript {filename="api.ts"}
// TypeScript API
interface ApiResponse<T> {
  data: T;
  status: number;
  message: string;
}

interface User {
  id: number;
  name: string;
  email: string;
  avatar?: string;
}

class ApiClient {
  private baseURL: string;
  private headers: Record<string, string>;

  constructor(baseURL: string, apiKey?: string) {
    this.baseURL = baseURL;
    this.headers = {
      'Content-Type': 'application/json',
      ...(apiKey && { 'Authorization': `Bearer ${apiKey}` })
    };
  }

  async get<T>(endpoint: string): Promise<ApiResponse<T>> {
    const response = await fetch(`${this.baseURL}${endpoint}`, {
      method: 'GET',
      headers: this.headers,
    });

    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }

    return response.json();
  }

  async post<T>(endpoint: string, data: any): Promise<ApiResponse<T>> {
    const response = await fetch(`${this.baseURL}${endpoint}`, {
      method: 'POST',
      headers: this.headers,
      body: JSON.stringify(data),
    });

    return response.json();
  }
}

const client = new ApiClient('https://api.example.com', 'your-api-key');

async function getUsers(): Promise<User[]> {
  try {
    const response = await client.get<User[]>('/users');
    return response.data;
  } catch (error) {
    console.error('Error fetching users:', error);
    return [];
  }
}
```


## Plain Text Codeblock

```
This is a plain text codeblock.
It should not have syntax highlighting.
You can test the copy functionality here.

function test() {
    console.log("This is a test.");
}
```

## Inline Code

This is an inline code example：`const x = 42;` and `npm install` and `git commit -m "update"`.

---

