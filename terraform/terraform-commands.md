# 🚀 Comandos Principales de Terraform

Esta guía contiene los 10 comandos más importantes de Terraform con sus explicaciones y ejemplos de uso.

---

## 1️⃣ `terraform init` 🏗️
**Inicializa un directorio de trabajo de Terraform**

```bash
terraform init
```

📝 **Explicación**: Descarga y configura los providers necesarios, inicializa el backend y prepara el directorio para usar Terraform.

🎯 **Cuándo usarlo**: Siempre que clones un nuevo proyecto o cambies la configuración de providers/backend.

---

## 2️⃣ `terraform plan` 📋
**Crea un plan de ejecución mostrando los cambios que se aplicarán**

```bash
terraform plan
terraform plan -out=plan.tfplan
```

📝 **Explicación**: Muestra qué recursos se crearán, modificarán o destruirán sin aplicar los cambios realmente.

🎯 **Cuándo usarlo**: Antes de aplicar cambios para revisar qué va a suceder.

---

## 3️⃣ `terraform apply` ✅
**Aplica los cambios requeridos para alcanzar la configuración deseada**

```bash
terraform apply
terraform apply plan.tfplan
terraform apply -auto-approve
```

📝 **Explicación**: Ejecuta las acciones propuestas en el plan de Terraform para crear/modificar/eliminar recursos.

🎯 **Cuándo usarlo**: Cuando estés listo para aplicar los cambios a tu infraestructura.

---

## 4️⃣ `terraform destroy` 💥
**Destruye todos los recursos gestionados por Terraform**

```bash
terraform destroy
terraform destroy -auto-approve
terraform destroy -target=resource.name
```

📝 **Explicación**: Elimina toda la infraestructura gestionada por la configuración actual de Terraform.

🎯 **Cuándo usarlo**: Para limpiar recursos de prueba o desmantelar infraestructura completamente.

---

## 5️⃣ `terraform validate` ✔️
**Valida la sintaxis y configuración de los archivos de Terraform**

```bash
terraform validate
```

📝 **Explicación**: Verifica que la configuración sea sintácticamente válida y consistente internamente.

🎯 **Cuándo usarlo**: Después de escribir o modificar archivos .tf para verificar errores básicos.

---

## 6️⃣ `terraform fmt` 🎨
**Formatea automáticamente los archivos de configuración**

```bash
terraform fmt
terraform fmt -recursive
terraform fmt -check
```

📝 **Explicación**: Aplica un formato consistente al código Terraform siguiendo las convenciones estándar.

🎯 **Cuándo usarlo**: Regularmente para mantener código limpio y consistente.

---

## 7️⃣ `terraform show` 👁️
**Muestra el estado actual o un plan guardado de manera legible**

```bash
terraform show
terraform show plan.tfplan
terraform show terraform.tfstate
```

📝 **Explicación**: Proporciona una salida legible para humanos del estado actual o de un plan específico.

🎯 **Cuándo usarlo**: Para inspeccionar el estado actual de recursos o revisar un plan guardado.

---

## 8️⃣ `terraform output` 📤
**Muestra los valores de salida de la configuración**

```bash
terraform output
terraform output instance_ip
terraform output -json
```

📝 **Explicación**: Extrae y muestra los valores de output definidos en tu configuración.

🎯 **Cuándo usarlo**: Para obtener información específica sobre recursos creados (IPs, URLs, etc.).

---

## 9️⃣ `terraform state` 🗂️
**Gestiona el archivo de estado de Terraform**

```bash
terraform state list
terraform state show resource.name
terraform state rm resource.name
terraform state mv old_name new_name
```

📝 **Explicación**: Permite inspeccionar y modificar el estado de Terraform para operaciones avanzadas.

🎯 **Cuándo usarlo**: Para debugging, migración de recursos o corrección de problemas de estado.

---

## 🔟 `terraform import` 📥
**Importa recursos existentes al estado de Terraform**

```bash
terraform import resource.name resource-id
terraform import aws_instance.example i-1234567890abcdef0
```

📝 **Explicación**: Trae recursos creados fuera de Terraform al control de tu configuración.

🎯 **Cuándo usarlo**: Para adoptar recursos existentes en tu gestión de infraestructura como código.

---

## 🎉 Tips Adicionales

### 🔧 Opciones Útiles Globales:
- `-var="key=value"` - Define variables
- `-var-file="file.tfvars"` - Carga archivo de variables  
- `-target=resource` - Aplica solo a recursos específicos
- `-parallelism=n` - Controla operaciones paralelas

### 📚 Workflow Recomendado:
1. `terraform init` 🏗️
2. `terraform validate` ✔️
3. `terraform fmt` 🎨
4. `terraform plan` 📋
5. `terraform apply` ✅

---

*💡 **Consejo**: Siempre revisa el plan antes de aplicar cambios en producción!*