---
name: Template
type: Matière
---
#GLO-2100 

Les templates permet de généraliser un type dans une classe.

### Exemple
---
Pour implémenter un template en c++
```cpp
template <typename T> // par convention le type est T
Class MyClass {

void set_member_var(const T var){
    general_type_var = var;
}

T get_member_var() const {
    return general_type_var;
}

private:
    T general_type_var;
}
```