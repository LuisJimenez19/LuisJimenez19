 # 👋 Hola, soy Luis
Soy un desarrollador web apasionado por construir sitios web con un diseño atractivo y una buena experiencia de usuario. Entre las herramientas con las que más disfruto trabajar estan tecnologías como ReactJS, Tailwind CSS + ViteJS y el stack MERN (MySQL, Express, React, Node.js). También he trabajado con Laravel e InertiaJS. Me emociona ver cómo la tendencia actual de unificar el desarrollo backend y frontend resalta la importancia de cada área.  



<section style="display: flex; justify-content: space-between; flex-wrap: wrap; gap: 20px;">
  <div>
    <img width="500px" src="https://github-readme-stats.vercel.app/api?username=luisjimenez19&show_icons=true&locale=es&theme=dracula&layout=compact" alt="luisjimenez19" />
  </div>
  <div>
    <img width="500px" src="https://github-readme-streak-stats.herokuapp.com?user=luisjimenez19&locale=es&theme=dracula&layout=compact" alt="luisjimenez19" />
  </div>
  <div>
    <img width="500px" src="https://github-readme-stats.vercel.app/api/top-langs?username=luisjimenez19&show_icons=true&locale=es&layout=compact&theme=dracula" alt="luisjimenez19" />
  </div>
</section>











## **Puedes encontrarme en internet**🌐  

- resolviendo desafios en [frontend mentor](https://www.frontendmentor.io/profile/LuisJimenez19)💯
- Aportando en [Linkedin](https://www.linkedin.com/in/luis-jimenez19/) 

### Te comparto;
- Mi [portafolio web](https://www.luis-dev.pro/) ♥ <br>
- Un simple portafolio de [desafios](https://luisjimenez19.github.io/desafios-frontend-mentor/) de frontend mentor.

¡Gracias por revisar mi perfil! Si tienes alguna pregunta o deseas colaborar en proyectos interesantes, no dudes en contactarme.


<!---
LuisJimenez19/LuisJimenez19 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

tour starter

```
import { setSteps, setIsOpen } from "@reactour/tour";
import { usersSteps } from "./users.tour";
import { groupsSteps } from "./groups.tour";
import { rolesSteps } from "./roles.tour";
import { clientsSteps } from "./clients.tour";
import { clientScopesSteps } from "./clientScopes.tour";
import { mappersSteps } from "./mappers.tour";

export const tourStarters = {
  users: () => {
    setSteps(usersSteps);
    setIsOpen(true);
  },
  groups: () => {
    setSteps(groupsSteps);
    setIsOpen(true);
  },
  roles: () => {
    setSteps(rolesSteps);
    setIsOpen(true);
  },
  clients: () => {
    setSteps(clientsSteps);
    setIsOpen(true);
  },
  clientScopes: () => {
    setSteps(clientScopesSteps);
    setIsOpen(true);
  },
  mappers: () => {
    setSteps(mappersSteps);
    setIsOpen(true);
  },
};

```


welcome tour

```
import { Button } from "@/components/ui/button";
import { tourStarters } from "./tourStarters";
import { useNavigate } from "react-router-dom";
import React from "react";

export const getDashboardTour = (navigate: ReturnType<typeof useNavigate>) => [
  {
    selector: "body",
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">
          👋 Bienvenido/a a la Consola Administrativa
        </h2>
        <p className="text-sm text-muted-foreground leading-relaxed">
          Esta aplicación te permite gestionar usuarios, grupos, permisos y
          clientes de manera simple, rápida y organizada.
          <br />
          <br />
          Empecemos con una vista general de lo que puedes hacer.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.cards"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">📌 ¿Qué puedes hacer aquí?</h2>
        <p className="text-sm text-muted-foreground leading-relaxed">
          Desde esta consola puedes crear cuentas, organizar usuarios, gestionar
          permisos y administrar aplicaciones vinculadas a la plataforma.
          <br />
          Todo está organizado por secciones para que encuentres fácilmente lo
          que necesitas.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.users"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">👤 Usuarios</h2>
        <p className="text-sm text-muted-foreground">
          Permite crear, editar y administrar cuentas de usuario.  
          También puedes asignar permisos, roles y grupos.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.groups"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">🧩 Grupos</h2>
        <p className="text-sm text-muted-foreground">
          Los grupos sirven para organizar usuarios y asignar permisos
          colectivos.  
          Facilita gestionar conjuntos grandes de usuarios.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.roles"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">🛡️ Roles</h2>
        <p className="text-sm text-muted-foreground">
          Los roles representan permisos específicos dentro del sistema.  
          Puedes asignarlos a usuarios o grupos según sus responsabilidades.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.clients"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">💼 Clientes</h2>
        <p className="text-sm text-muted-foreground">
          Un cliente representa una aplicación que utiliza esta plataforma para
          autenticar usuarios y aplicar permisos.  
          Desde aquí puedes ver sus configuraciones y roles asociados.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.clientScopes"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">🔧 Client Scopes</h2>
        <p className="text-sm text-muted-foreground">
          Un client scope es un conjunto de configuraciones reutilizables que se
          pueden asociar a múltiples clientes.  
          Controla qué información se envía al iniciar sesión o autorizar.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.mappers"]',
    content: () => (
      <div>
        <h2 className="text-lg font-semibold mb-2">🧱 Mappers</h2>
        <p className="text-sm text-muted-foreground">
          Los mappers definen qué datos se incluyen en los tokens y respuestas
          de autorización.  
          Pueden tomar valores del usuario o valores fijos según tu necesidad.
        </p>
      </div>
    ),
  },

  {
    selector: '[data-tour="dashboard.footer"]',
    content: () => (
      <div className="space-y-4">
        <h2 className="text-lg font-semibold mb-1">
          🎉 ¡Tour inicial completado!
        </h2>
        <p className="text-sm text-muted-foreground leading-relaxed">
          Ya conoces la estructura general de la consola.  
          Si deseas explorar más en detalle cada módulo, elige uno para
          continuar:
        </p>

        <div className="grid grid-cols-1 gap-2 mt-4">
          <Button
            variant="outline"
            onClick={() => {
              navigate("/users");
              tourStarters.users();
            }}
          >
            👤 Tour de Usuarios
          </Button>

          <Button
            variant="outline"
            onClick={() => {
              navigate("/groups");
              tourStarters.groups();
            }}
          >
            🧩 Tour de Grupos
          </Button>

          <Button
            variant="outline"
            onClick={() => {
              navigate("/roles");
              tourStarters.roles();
            }}
          >
            🛡️ Tour de Roles
          </Button>

          <Button
            variant="outline"
            onClick={() => {
              navigate("/clients");
              tourStarters.clients();
            }}
          >
            💼 Tour de Clientes
          </Button>

          <Button
            variant="outline"
            onClick={() => {
              navigate("/client-scopes");
              tourStarters.clientScopes();
            }}
          >
            🔧 Tour de Client Scopes
          </Button>

          <Button
            variant="outline"
            onClick={() => {
              navigate("/mappers");
              tourStarters.mappers();
            }}
          >
            🧱 Tour de Mappers
          </Button>
        </div>
      </div>
    ),
  },
];
```


selectores

```
<div data-tour="dashboard.cards">...</div>

<Link to="/users" data-tour="dashboard.users">...</Link>

<Link to="/groups" data-tour="dashboard.groups">...</Link>

<Link to="/roles" data-tour="dashboard.roles">...</Link>

<Link to="/clients" data-tour="dashboard.clients">...</Link>

<Link to="/client-scopes" data-tour="dashboard.clientScopes">...</Link>

<Link to="/mappers" data-tour="dashboard.mappers">...</Link>

<footer data-tour="dashboard.footer">...</footer>

```


users tour
```
import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { Button } from "@/components/ui/button";
import { EMOJIS } from "@/constants/emojis";

export const usersSteps: StepType[] = [
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.users} Gestión de Usuarios`} />
        <Paragraph text="En esta sección puedes administrar todas las cuentas del sistema: crear usuarios, editar información, modificar permisos y organizarlos en grupos." />
        <Footer text="Veamos cada parte de esta pantalla." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Título de la sección" />
        <Paragraph text="Aquí siempre podrás ver en qué módulo te encuentras. En este caso, estás administrando usuarios." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.table.filters"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Filtros y herramientas" />
        <Paragraph text="Puedes buscar usuarios por nombre de usuario y ajustar cuántos resultados se muestran por página." />
        <Footer text="Ideal para trabajar con listas largas." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.create"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Crear un nuevo usuario" />
        <Paragraph text="Aquí puedes añadir una nueva cuenta completando un formulario con información básica como nombre, apellido y correo electrónico." />
        <Footer text="La creación rápida te permite mantener el control del sistema." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.addToGroup"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Agregar usuarios a un grupo" />
        <Paragraph text="Selecciona varios usuarios y asígnalos a un grupo. Es útil cuando administras grandes equipos o áreas." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Lista de usuarios" />
        <Paragraph text="Aquí ves todos los usuarios registrados, junto con su información principal: email, nombres, estado y roles asignados." />
        <Footer text="Cada fila representa una cuenta del sistema." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones disponibles" />
        <Paragraph text="Desde aquí puedes editar datos del usuario, asignar roles, añadirlo a grupos, gestionar sus atributos e incluso cambiar su contraseña." />
        <Footer text="Todo al alcance de un clic." />
      </div>
    ),
  },

  {
    selector: '[data-tour="users.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Navega entre las páginas de resultados. Esto es especialmente útil cuando administras cientos o miles de usuarios." />
        <Footer text="Y listo. Con esto ya conoces la gestión de usuarios." />
      </div>
    ),
  },
];




<h1 data-tour="users.title">Usuarios</h1>

<div data-tour="users.table.filters">...</div>

<button data-tour="users.create">Crear nuevo usuario</button>

<button data-tour="users.addToGroup">Agregar a grupo</button>

<table data-tour="users.table">...</table>

<div data-tour="users.table.actions">...</div>

<div data-tour="users.table.pagination">...</div>



{
  selector: "body",
  content: () => (
    <div>
      <Title text="¿Quieres seguir explorando?" />
      <Paragraph text="Puedes continuar con otras secciones del sistema para conocer todas las funcionalidades disponibles." />
      <div className="flex flex-col mt-3 gap-2">
        <Button onClick={() => tourStarters.groups()}>Tour de Grupos</Button>
        <Button onClick={() => tourStarters.roles()}>Tour de Roles</Button>
        <Button onClick={() => tourStarters.clients()}>Tour de Clientes</Button>
      </div>
    </div>
  ),
}
```



###Grupos

<h1 data-tour="groups.title">Grupos</h1>

<div data-tour="groups.filters">...</div>

<button data-tour="groups.create">Crear nuevo grupo</button>

<table data-tour="groups.table">...</table>

<div data-tour="groups.table.actions">...</div>

<div data-tour="groups.table.pagination">...</div>






import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const groupsSteps: StepType[] = [
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.groups} Gestión de Grupos`} />
        <Paragraph text="Aquí puedes crear y organizar grupos para estructurar usuarios según equipos, áreas o necesidades específicas." />
        <Footer text="Vamos a recorrer cada parte de la pantalla." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Título de la sección" />
        <Paragraph text="Esta es la vista principal para administrar los grupos existentes dentro de la plataforma." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.filters"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Filtros disponibles" />
        <Paragraph text="Puedes buscar grupos por nombre y ajustar cuántos resultados ver por página. Perfecto para entornos con muchos equipos." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.create"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Crear nuevo grupo" />
        <Paragraph text="Desde aquí puedes añadir un grupo completamente nuevo. Solo necesitas asignarle un nombre." />
        <Footer text="Una forma rápida de estructurar mejor tus usuarios." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Listado de grupos" />
        <Paragraph text="Aquí verás todos los grupos creados, junto con accesos directos para administrarlos: editar información, gestionar roles y explorar diagramas." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones disponibles" />
        <Paragraph text="Cada grupo tiene accesos rápidos para editarlo, asignar roles globales, asignar roles de cliente, visualizar el diagrama y eliminar el grupo." />
        <Footer text="Todas las herramientas de administración organizadas en un solo lugar." />
      </div>
    ),
  },

  {
    selector: '[data-tour="groups.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Controla la navegación entre páginas cuando tienes muchos grupos creados." />
        <Footer text="Y listo, ya conoces la gestión de grupos." />
      </div>
    ),
  },
];



{
  selector: "body",
  content: () => (
    <div>
      <Title text="¿Quieres continuar?" />
      <Paragraph text="Puedes explorar los tours de otras secciones para entender el sistema por completo." />
      <div className="flex flex-col mt-3 gap-2">
        <Button onClick={() => tourStarters.users()}>Tour de Usuarios</Button>
        <Button onClick={() => tourStarters.roles()}>Tour de Roles</Button>
        <Button onClick={() => tourStarters.clients()}>Tour de Clientes</Button>
      </div>
    </div>
  ),
}