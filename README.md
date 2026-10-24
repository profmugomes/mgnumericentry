# MGNumericEntry

[![License](https://img.shields.io/badge/license-MIT-5351FB)](LICENSE)

Um componente customizado para **Fyne (Go)** que fornece um **campo de entrada numérica** com validação, limites (min/max), incremento/decremento e **botões de spin com auto-repeat** (pressionar e segurar).

Ideal para formulários, configurações e interfaces desktop que precisam de controle numérico preciso.

---

## ✨ Recursos

* 🔢 Entrada **somente numérica**
* ➕➖ Incremento e decremento com passo configurável
* ⏫⏬ Botões de spin (▲ / ▼) com **auto-repeat**
* 🔒 Respeita valores mínimos e máximos
* 🔄 Callback `OnChanged` ao alterar valor
* 🖱️ Suporte a mouse, teclado e foco

---

## 📦 Instalação

```bash
go get github.com/profmugomes/mgnumericentry
```

---

## 🚀 Uso básico

### Numeric Entry simples

```go
entry := mgnumericentry.NewMGNumericEntry(0, 100, 10)

entry.OnChanged = func(v int) {
	fmt.Println("Valor alterado:", v)
}
```

---

### Numeric Entry com botões de incremento/decremento

```go
box, entry := mgnumericentry.NewMGNumericEntryWithButtons(0, 100, 5)

entry.OnChanged = func(v int) {
	fmt.Println("Novo valor:", v)
}

w.SetContent(box)
```

---

## ⚙️ Propriedades principais

### `MGNumericEntry`

| Campo       | Tipo        | Descrição                      |
| ----------- | ----------- | ------------------------------ |
| `Min`       | `int`       | Valor mínimo permitido         |
| `Max`       | `int`       | Valor máximo permitido         |
| `Value`     | `int`       | Valor atual                    |
| `OnChanged` | `func(int)` | Callback ao alterar o valor    |

---

## 🧠 Métodos úteis

```go
entry.GetValue()
entry.SetValue(42)
```

---

## 🧩 Compatibilidade

* Go 1.27.2+
* Fyne 2.8.0

---

## 👤 Autor

**Murilo Gomes**

🔗 [https://www.profmugomes.com.br](https://www.profmugomes.com.br)

📺 [https://youtube.com/@profmugomes](https://youtube.com/@profmugomes)

---

## License

Copyright (c) 2025-2026 Murilo Gomes <profmugomes.com.br>

Licensed under the [MIT](https://github.com/profmugomes/mgnumericentry/blob/main/LICENSE) license.

All contributions to the MGNumericEntry are subject to this license.
