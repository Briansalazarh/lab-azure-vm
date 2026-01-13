# lab-azure-vm
Documentação prática sobre a criação de Máquinas Virtuais no Microsoft Azure.
# Desafío: Creación de una Máquina Virtual en Azure

Este repositorio contiene la documentación paso a paso para la creación y configuración de una Máquina Virtual (VM) con Windows Server en Microsoft Azure.

## Objetivo
Demostrar la capacidad de aprovisionar infraestructura en la nube (IaaS), configurando recursos de red, seguridad y computación.

## Paso a Paso Realizado

### 1. Acceso y Configuración Inicial
* Acceso al [Portal de Azure](https://portal.azure.com).
* En el menú de servicios, selección de **Virtual Machines** (Máquinas Virtuales) y clic en **Create** > **Azure virtual machine**.

### 2. Configuraciones Básicas (Basics)
Se definieron los campos obligatorios para la identidad de la VM:
* **Subscription:** Suscripción utilizada para el laboratorio.
* **Resource Group:** Creación de un nuevo grupo llamado `rg-lab-azure` para organizar los recursos.
* **Virtual Machine Name:** `vm-windows-server`.
* **Region:** `East US` (EUA Este), seleccionada por disponibilidad y costo.
* **Availability Options:** Sin redundancia de infraestructura (configuración para pruebas).
* **Image:** `Windows Server 2019 Datacenter - x64 Gen2`.
* **Size:** `Standard_B1s` (o B2s), adecuado para pruebas de bajo costo.

### 3. Cuenta de Administrador
Configuración de las credenciales de acceso:
* **Username:** `azureuser`
* **Password:** Definición de una contraseña segura siguiendo las políticas de complejidad.

### 4. Reglas de Puerto de Entrada (Networking)
Para permitir el acceso remoto, se configuraron los puertos públicos:
* **Public inbound ports:** Allow selected ports.
* **Select inbound ports:** `RDP (3389)`, esencial para acceder a Windows de forma remota.

### 5. Revisión y Creación
* Se mantuvieron las configuraciones por defecto en las pestañas de Discos (SSD), Redes y Administración.
* En la pestaña **Review + create**, Azure validó las configuraciones.
* Clic en **Create**. El despliegue se completó en pocos minutos.

### 6. Conexión (Connect)
* Con el recurso en estado "Running", clic en **Connect** > **RDP**.
* Descarga del archivo `.rdp`.
* Acceso mediante el archivo descargado utilizando las credenciales de administrador creadas anteriormente.
* ¡Acceso exitoso al escritorio remoto de Windows Server!

## Aprendizajes
* **Resource Groups:** La importancia de agrupar recursos para facilitar la gestión y eliminación masiva.
* **Regiones:** Cómo la elección de la región impacta directamente en la latencia y el costo del servicio.
* **Seguridad:** La necesidad de habilitar el puerto 3389 (RDP) solo cuando sea necesario o restringirlo a IPs específicas en entornos de producción.

# Desafio: Criando uma Máquina Virtual no Azure

Este repositório contém a documentação do passo a passo para a criação e configuração de uma Máquina Virtual (VM) com Windows Server no Microsoft Azure.

## Objetivo
Demonstrar a capacidade de provisionar infraestrutura na nuvem (IaaS), configurando recursos de rede, segurança e computação.

## Passo a Passo Realizado

### 1. Acesso e Configuração Inicial
* Acessei o [Portal do Azure](https://portal.azure.com).
* No menu de serviços, selecionei **Virtual Machines** (Máquinas Virtuais) e cliquei em **Create** > **Azure virtual machine**.

### 2. Configurações Básicas (Basics)
Preenchi os campos obrigatórios para definir a identidade da VM:
* **Subscription:** Assinatura utilizada para o laboratório.
* **Resource Group:** Criei um novo grupo chamado `rg-azure-lab` para organizar os recursos.
* **Virtual Machine Name:** `vm-windows-server`.
* **Region:** `East US` (EUA Leste) - selecionada por custo e disponibilidade.
* **Availability Options:** No infrastructure redundancy required (configuração para testes).
* **Image:** `Windows Server 2019 Datacenter - x64 Gen2`.
* **Size:** `Standard_B1s` (ou B2s), adequado para testes de baixo custo.

### 3. Conta de Administrador
Configurei as credenciais de acesso:
* **Username:** `azureuser`
* **Password:** Senha forte definida seguindo as políticas de complexidade.

### 4. Regras de Porta de Entrada (Networking)
Para permitir o acesso remoto, configurei as portas públicas:
* **Public inbound ports:** Allow selected ports.
* **Select inbound ports:** `RDP (3389)` - Essencial para acessar Windows remotamente.

### 5. Revisão e Criação
* Avancei pelas abas de Discos (SSD), Networking e Management mantendo as configurações padrão recomendadas para este cenário.
* Na aba **Review + create**, o Azure validou as configurações.
* Cliquei em **Create**. O deployment levou alguns minutos para ser concluído.

### 6. Conexão (Connect)
* Após o recurso estar "Running", cliquei em **Connect** > **RDP**.
* Baixei o arquivo `.rdp`.
* Abri o arquivo e entrei com as credenciais de Administrador criadas no passo 3.
* Sucesso! Acesso à área de trabalho remota do Windows Server garantido.

## Aprendizados
* **Resource Groups:** A importância de agrupar recursos para facilitar a gestão e exclusão posterior.
* **Regiões:** A escolha da região impacta diretamente na latência e no custo.
* **Segurança:** A necessidade de liberar a porta 3389 (RDP) apenas quando necessário ou restringir a IPs específicos em ambientes de produção.
