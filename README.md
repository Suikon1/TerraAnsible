# TFLEO - DevOps Project

**Proyecto completo de DevOps que integra Terraform, Ansible y SpringBoot para automatización de infraestructura y despliegue de aplicaciones.**

## 📋 Descripción del Proyecto

Este repositorio contiene un proyecto integral de DevOps que combina:

- **🏗️ Terraform**: Infraestructura como código (IaC) para aprovisionamiento de recursos en la nube
- **⚙️ Ansible**: Automatización de configuración y gestión de servidores
- **🚀 SpringBoot**: API REST para ventas con arquitectura moderna

## 🗂️ Estructura del Proyecto

```
TFLEO/
├── 📁 Terraform/           # Infraestructura como código
│   ├── main.tf            # Configuración principal de Terraform
│   └── ...                # Otros archivos de configuración
├── 📁 Ansible/            # Automatización y configuración
│   ├── playbooks/         # Playbooks de Ansible
│   ├── inventory/         # Inventario de servidores
│   └── roles/             # Roles reutilizables
└── 📁 API_REST_Ventas_SpringBoot/  # Aplicación Spring Boot
    ├── src/               # Código fuente
    ├── pom.xml           # Dependencias Maven
    └── ...               # Configuración de la aplicación
```

## 🚀 Tecnologías Utilizadas

### Infrastructure as Code
- **Terraform** - Aprovisionamiento de infraestructura
- **AWS/Azure/GCP** - Proveedores de nube

### Configuration Management
- **Ansible** - Automatización de configuración
- **YAML** - Definición de playbooks

### Application Development
- **Java 17+** - Lenguaje de programación
- **Spring Boot 3.x** - Framework de aplicación
- **Spring Data JPA** - Persistencia de datos
- **Maven** - Gestión de dependencias
- **MySQL/PostgreSQL** - Base de datos

### DevOps Tools
- **Git** - Control de versiones
- **GitHub** - Repositorio remoto
- **SSH** - Conexión segura a servidores

## 📋 Prerrequisitos

### Para Terraform
```bash
# Instalar Terraform
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install terraform
```

### Para Ansible
```bash
# Instalar Ansible
sudo apt update
sudo apt install ansible
```

### Para SpringBoot
```bash
# Java 17+
sudo apt install openjdk-17-jdk

# Maven
sudo apt install maven
```

## 🛠️ Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/Suikon1/TFLEO.git
cd TFLEO
```

### 2. Configurar Terraform
```bash
cd Terraform/
terraform init
terraform plan
terraform apply
```

### 3. Configurar Ansible
```bash
cd ../Ansible/
# Editar inventory con las IPs de tus servidores
ansible-playbook -i inventory playbook.yml
```

### 4. Ejecutar SpringBoot
```bash
cd ../API_REST_Ventas_SpringBoot/
mvn clean install
mvn spring-boot:run
```

## 🔧 Uso del Proyecto

### Despliegue de Infraestructura
1. **Configurar credenciales** de tu proveedor de nube
2. **Personalizar variables** en `terraform.tfvars`
3. **Ejecutar Terraform** para crear la infraestructura
4. **Anotar las IPs** de los servidores creados

### Configuración de Servidores
1. **Actualizar inventory** de Ansible con las nuevas IPs
2. **Ejecutar playbooks** para configurar los servidores
3. **Verificar conectividad** y servicios

### Despliegue de Aplicación
1. **Compilar** la aplicación SpringBoot
2. **Configurar** base de datos y variables de entorno
3. **Desplegar** usando Ansible o manualmente
4. **Verificar** que la API esté funcionando

## 📊 API Endpoints

La API REST de ventas incluye los siguientes endpoints:

```
GET    /api/ventas          # Listar todas las ventas
POST   /api/ventas          # Crear nueva venta
GET    /api/ventas/{id}     # Obtener venta por ID
PUT    /api/ventas/{id}     # Actualizar venta
DELETE /api/ventas/{id}     # Eliminar venta
```

## 🔒 Seguridad

- **Archivos sensibles** (.pem, .key) están excluidos del repositorio
- **Variables de entorno** para credenciales
- **SSH keys** para acceso seguro a servidores
- **HTTPS** recomendado para producción

## 🧪 Testing

```bash
# Validar Terraform
terraform validate
terraform plan

# Verificar sintaxis Ansible
ansible-playbook --syntax-check playbook.yml

# Test SpringBoot
mvn test
```

## 📈 Monitoreo y Logs

- **Logs de aplicación**: `logs/application.log`
- **Logs de sistema**: `/var/log/syslog`
- **Métricas**: Configurar Prometheus/Grafana (opcional)

## 🤝 Contribución

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📝 Notas Importantes

- **Nunca commitear** archivos `.pem` o credenciales
- **Usar variables de entorno** para configuración sensible
- **Revisar costos** antes de aplicar Terraform en producción
- **Hacer backup** de estados de Terraform

## 📞 Soporte

Si tienes preguntas o problemas:

1. Revisa la documentación de cada tecnología
2. Consulta los logs de error
3. Abre un issue en este repositorio

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

**Desarrollado con ❤️ para aprender DevOps**

### 🔗 Enlaces Útiles

- [Documentación de Terraform](https://www.terraform.io/docs)
- [Documentación de Ansible](https://docs.ansible.com/)
- [Documentación de Spring Boot](https://spring.io/projects/spring-boot)
- [Guías de AWS](https://docs.aws.amazon.com/)
