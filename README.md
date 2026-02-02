# 📚 Funcions en Python

Una guia completa sobre la creació i utilització de funcions en Python, amb exemples pràctics en català.

## 📋 Taula de Continguts

- [Introducció](#introducció)
- [Creació de Funcions](#creació-de-funcions)
- [Pas de Paràmetres](#pas-de-paràmetres)
- [Valor de Retorn](#valor-de-retorn)
- [Valors per Defecte](#valors-per-defecte)
- [Exemples](#exemples)

## 🎯 Introducció

Una funció és un bloc de codi reutilitzable que només s'executa quan el crides. Utilitzem la paraula clau `def` per definir-la.

**Objectiu:** Evitar repetir codi i fer el programa més net.

**Sintaxi:** `def`, nom de la funció, parèntesis `()` i dos punts `:`. Tot el codi de dins ha d'estar indentat.

## 🔧 Creació de Funcions

### Exemple: Funció que saluda

```python
# Definició de la funció
def say_hello():
    print("Hello!")

# Crida de la funció
say_hello()
```

## 📦 Pas de Paràmetres

Els paràmetres són variables que posem dins dels parèntesis. Permeten que la funció treballi amb dades diferents cada vegada que la cridem.

- **Paràmetre:** El nom de la variable que farem servir a la funció (podem posar el nom que vulguem, però hem d'intentar que tingui coherència)
- **Argument:** El valor real que passem quan la cridem
- **Observació:** L'ordre és important a la crida, cada espai indica la posició amb la qual la rep la funció

### Exemple: Funció amb paràmetres

```python
def say_hello_user(username, age):
    print(f"Hello {username}, you are {age} old.")

# Crida per posició
say_hello_user("Detectiu Conan", 16)

# Crida per nom (l'ordre no importa)
say_hello_user(age=16, username="Detectiu Conan")
```

> ⚠️ **ATENCIÓ:** També podem passar els arguments pel seu nom i l'ordre no importarà!

## 🔄 Valor de Retorn

### Diferència clau

- **`print`:** Només mostra text a la pantalla (per a l'usuari)
- **`return`:** Retorna la dada al programa perquè la puguis guardar en una variable o fer càlculs posteriors

> ⚡ **Regla:** Quan Python llegeix un `return`, la funció s'acaba immediatament!

### Exemple: Funció amb return

```python
def calculate_price(price, tax):
    total = price * tax
    return total

# Emmagatzemar el resultat en una variable
result = calculate_price(10, 5)
print(f"El preu final és: {result}")

# Mostrar directament el valor
print(f"El preu final és: {calculate_price(10, 5)}")

# Avaluar el resultat en una estructura de control
if calculate_price(10, 5) > 10:
    print("El preu és major a 10")
else:
    print("El preu és menor a 10")
```

## ⚙️ Valors per Defecte

Pots fer que certs paràmetres siguin opcionals assignant-los un valor inicial amb `=`.

> 📌 **Regla:** Els paràmetres amb valor per defecte han d'anar sempre al final, després dels obligatoris.

### Exemple: Funció amb valors per defecte

```python
def display_price(price, currency="€"):
    print(f"El preu és {price}{currency}")

# Fer servir el valor per defecte
display_price(10)  # Output: El preu és 10€

# Modificar el valor per defecte
display_price(10, "$")  # Output: El preu és 10$
```

## 💡 Exemples

### Exemple complet

```python
def calculate_discount(price, discount=10):
    """
    Calcula el preu final amb descompte aplicat
    
    Args:
        price (float): Preu original del producte
        discount (int): Percentatge de descompte (per defecte 10%)
    
    Returns:
        float: Preu final amb descompte aplicat
    """
    final_price = price - (price * discount / 100)
    return final_price

# Utilitzar la funció
print(f"Preu amb 10% descompte: {calculate_discount(100)}€")
print(f"Preu amb 20% descompte: {calculate_discount(100, 20)}€")
```

---

Fet amb ❤️ per a estudiants de Python
