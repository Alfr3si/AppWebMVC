# Proyecto de .Net, Razor y Entity Framework

## Descripcion

Este proyecto se creo con la finalidad de crear una aplicacion web con Razor y Entity Framework la cual sea capaz de ....
Hasta ahora lo que debe de hacer el proyecto es:

- crear un login, y acceso a los usuarios
- crear la base de datos
- actualizar la base de datos con el proyecto

## Instalacion

Para ese apartado me enfoque en la compataibilidad entre la version de .NET 9.0 ya que el docente nos dio la posibilidad de
trabajar con cualquier version de .NET 9.0 o posterior.

---

### Debian 13

> [!IMPORTANT]
> Agregar Repositorios de Microsoft

```bash
# esto debido a que aun no hay empaquetado para la version de debian 13 por eso usamos la 12
wget https://packages.microsoft.com/config/debian/13/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update

```

Instalar .NET SDK 9.0

```bash
sudo apt-get install dotnet-sdk-9.0

```

Verificar Instalacion

```bash
dotnet --version
dotnet --list-sdks
dotnet --list-runtimes

```

Instalar los paquetes NuGet Necesarios

```bash

dotnet add package Microsoft.AspNetCore.Identity.UI
dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.Tools

```

Ejecutar Proyecto

```bash
cd ~/Proyectos/dotnet/AppWebMVC
dotnet restore
dotnet run

```

---

### Arch Linux

Instalacion del SDK 9.0

> [!NOTE]
> Descargala desde:
> https://dotnet.microsoft.com/en-us/download/dotnet/9.0

Descomprimir en ~/.dotnet

```bash
mkdir -p ~/.dotnet
tar -xzf dotnet-sdk-9.0.x-linux-x64.tar.gz -C ~/.dotnet

```

Agreegar al PATH

```bash
export DOTNET_ROOT=$HOME/.dotnet
export PATH=$DOTNET_ROOT:$PATH

```

Verificar la Instalacion

```bash
dotnet --list-sdks
dotnet --list-runtimes

```

---

## Desarrollo
