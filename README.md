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

```

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


```


### Clientes

```

<h1 data-tour="clients.title">Clientes</h1>

<div data-tour="clients.filters">...</div>

<div className="flex items-center gap-2" data-tour="clients.actions">
  <button>Crear nuevo cliente</button>
  <button>Client scopes</button> {/* o un link */}
</div>

<table data-tour="clients.table">...</table>

<div data-tour="clients.table.actions">...</div>

<div data-tour="clients.table.pagination">...</div>




import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const clientsSteps: StepType[] = [
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.clients} Gestión de Clientes`} />
        <Paragraph text="Los clientes representan aplicaciones o servicios que se conectan a la plataforma y necesitan autenticación, permisos y reglas personalizadas." />
        <Footer text="Veamos cómo administrar los clientes disponibles." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Página de Clientes" />
        <Paragraph text="Aquí encontrarás todas las aplicaciones registradas dentro de la plataforma, junto con sus configuraciones más importantes." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.filters"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Filtros" />
        <Paragraph text="Puedes buscar clientes por ID y ajustar el número de resultados para encontrar más rápido la aplicación que necesitas." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones principales" />
        <Paragraph text="Desde aquí puedes crear un nuevo cliente o acceder al catálogo de Client Scopes disponibles en la plataforma." />
        <Footer text="Ideal para administrar aplicaciones y sus permisos asociados." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Listado de Clientes" />
        <Paragraph text="Cada fila representa una aplicación configurada. Puedes ver su estado, editarla y administrar roles, scopes, mappers y credenciales." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones por cliente" />

        <Paragraph text="Cada cliente tiene acciones específicas:" />

        <Paragraph
          text={`
• Editar: cambiar nombre, protocolo o configuraciones básicas.  
• Roles: administrar los roles que la aplicación puede asignar.  
• Scopes: definir qué información es accesible desde la app.  
• Mappers: personalizar qué atributos se exponen al autenticarse.  
• Diagramas: visualizar la estructura y conexiones del cliente.  
• Credenciales: gestionar secretos y configuraciones de acceso.  
• Eliminar: borrar el cliente de la plataforma.
          `}
        />

        <Footer text="Todo lo necesario para administrar aplicaciones de forma segura y ordenada." />
      </div>
    ),
  },

  {
    selector: '[data-tour="clients.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Navega entre las páginas para ver todos los clientes configurados." />
        <Footer text="¡Listo! Ya conoces la sección de Clientes." />
      </div>
    ),
  },
];



{
  selector: "body",
  content: () => (
    <div>
      <Title text="¿Quieres continuar con otro tour?" />
      <Paragraph text="Puedes explorar otras secciones para conocer más sobre la plataforma." />
      <div className="flex flex-col gap-2 mt-3">
        <Button onClick={() => goToTour("users")}>Usuarios</Button>
        <Button onClick={() => goToTour("groups")}>Grupos</Button>
        <Button onClick={() => goToTour("roles")}>Roles</Button>
        <Button onClick={() => goToTour("client-scopes")}>Client Scopes</Button>
      </div>
    </div>
  ),
}
```


### roles


```
<h1 data-tour="roles.title">Roles</h1>

<div data-tour="roles.roleTypeSelector">...</div>

<div data-tour="roles.filters">...</div>

<div data-tour="roles.actions">...</div>

<table data-tour="roles.table">...</table>

<div data-tour="roles.table.actions">...</div>

<div data-tour="roles.table.pagination">...</div>





import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const rolesSteps: StepType[] = [
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.roles} Roles`} />
        <Paragraph text="En esta sección puedes administrar los permisos disponibles dentro de la plataforma, tanto roles globales como roles asociados a clientes específicos." />
        <Footer text="Primero veamos cómo está organizada la pantalla." />
      </div>
    ),
  },

  {
    selector: '[data-tour="roles.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Administración de Roles" />
        <Paragraph text="Aquí puedes gestionar los roles disponibles, organizarlos, editarlos y asignarlos a usuarios o grupos." />
      </div>
    ),
  },

  // SELECTOR GLOBAL / CLIENT
  {
    selector: '[data-tour="roles.roleTypeSelector"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Tipos de Roles" />

        <Paragraph
          text={`
Esta plataforma maneja dos tipos de roles:

• **Roles Globales**: afectan a toda la plataforma.  
• **Client Roles**: roles pertenecientes a una aplicación específica.

Puedes alternar entre ellos usando este selector.
        `}
        />

        <Footer text="Cambia entre vistas según lo que necesites administrar." />
      </div>
    ),
  },

  // FILTERS
  {
    selector: '[data-tour="roles.filters"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Filtros" />
        <Paragraph text="Filtra roles por nombre y ajusta la cantidad de filas a mostrar por página." />
      </div>
    ),
  },

  // ACTIONS
  {
    selector: '[data-tour="roles.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones principales" />
        <Paragraph text="Puedes crear nuevos roles globales, o asignar roles (globales o de cliente) a usuarios y grupos." />
        <Footer text="Es una forma rápida de administrar permisos a gran escala." />
      </div>
    ),
  },

  // TABLE GENERAL
  {
    selector: '[data-tour="roles.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Listado de Roles" />
        <Paragraph text="Aquí verás todos los roles disponibles según la vista seleccionada (global o de cliente)." />
      </div>
    ),
  },

  // TABLE ACTIONS
  {
    selector: '[data-tour="roles.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones por Rol" />

        <Paragraph
          text={`
Cada rol tiene acciones específicas según su tipo:

• **Editar**: cambia nombre o información del rol.  
• **Usuarios**: asigna o quita este rol a usuarios.  
• **Grupos**: asigna o quita este rol a grupos.  
• **Eliminar**: solo para roles globales o roles de cliente creados por el usuario.
          `}
        />

        <Footer text="Permite administrar permisos de manera detallada." />
      </div>
    ),
  },

  // PAGINATION
  {
    selector: '[data-tour="roles.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Navega entre páginas para ver todos los roles disponibles." />
        <Footer text="Listo. Ya conoces la sección de Roles." />
      </div>
    ),
  },
];

```



### client scopes

```
<h1 data-tour="client-scopes.title">Client Scopes</h1>

<div data-tour="client-scopes.filters">...</div>

<div data-tour="client-scopes.actions">...</div>

<table data-tour="client-scopes.table">...</table>

<div data-tour="client-scopes.table.actions">...</div>

<div data-tour="client-scopes.table.pagination">...</div>





import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const clientScopesSteps: StepType[] = [
  // INTRO
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.scopes} Client Scopes`} />
        <Paragraph
          text={`
Los Client Scopes son conjuntos de atributos y configuraciones que
pueden añadirse a uno o varios clientes para ampliar la información
que reciben durante la autenticación.
          `}
        />
        <Footer text="Veamos cómo funciona esta sección." />
      </div>
    ),
  },

  // TITLE
  {
    selector: '[data-tour="client-scopes.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Administración de Client Scopes" />
        <Paragraph text="Aquí puedes ver, crear, editar y gestionar scopes utilizados por los clientes de la plataforma." />
      </div>
    ),
  },

  // FILTERS
  {
    selector: '[data-tour="client-scopes.filters"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Filtros" />
        <Paragraph text="Filtra los scopes por nombre y ajusta cuántos elementos ver por página." />
      </div>
    ),
  },

  // ACTIONS
  {
    selector: '[data-tour="client-scopes.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Crear nuevo Scope" />
        <Paragraph
          text={`
Puedes crear un nuevo Client Scope.  
Durante la creación deberás definir su nombre, descripción y protocolo.
          `}
        />
        <Footer text="Algunos scopes pueden estar limitados por el protocolo." />
      </div>
    ),
  },

  // TABLE
  {
    selector: '[data-tour="client-scopes.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Listado de Scopes" />
        <Paragraph
          text={`
Cada fila representa un Client Scope disponible en la plataforma.
Estos scopes pueden ser reutilizados por múltiples clientes.
          `}
        />
      </div>
    ),
  },

  // TABLE ACTIONS
  {
    selector: '[data-tour="client-scopes.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones por Scope" />

        <Paragraph
          text={`
• **Editar**: modifica nombre, descripción y configuración básica.  
• **Mappers**: administra qué atributos o datos se incluyen dentro del scope.  
• **Eliminar**: disponible solo para scopes creados por el usuario.
          `}
        />

        <Footer text="Los mappers son claves para definir qué información viaja en el token." />
      </div>
    ),
  },

  // PAGINATION
  {
    selector: '[data-tour="client-scopes.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Usa los controles para navegar entre los scopes disponibles." />
        <Footer text="Listo. Ya conoces la sección de Client Scopes." />
      </div>
    ),
  },
];

```


### Mappers

```
<h1 data-tour="mappers.title">Mappers</h1>

<div data-tour="mappers.description"></div>

<div data-tour="mappers.actions"></div>

<table data-tour="mappers.table"></table>

<div data-tour="mappers.table.actions"></div>

<div data-tour="mappers.table.pagination"></div>






import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const mappersSteps: StepType[] = [
  // INTRO
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.mappers} Mappers`} />
        <Paragraph
          text={`
Los Mappers definen qué información del usuario o del sistema
se incluye dentro del token generado durante la autenticación.
          `}
        />
        <Footer text="Veamos cómo funciona esta sección." />
      </div>
    ),
  },

  // TITLE
  {
    selector: '[data-tour="mappers.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Administración de Mappers" />
        <Paragraph
          text={`
Aquí puedes crear, editar y eliminar mappers.  
Cada mapper representa una regla que indica qué dato debe agregarse
al token final.
          `}
        />
      </div>
    ),
  },

  // GENERAL DESCRIPTION (OPTIONAL)
  {
    selector: '[data-tour="mappers.description"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="¿Qué es un Mapper?" />

        <Paragraph
          text={`
Un mapper define cómo un atributo debe transformarse o enviarse dentro
de un token de autenticación.

Existen distintos tipos de mappers, por ejemplo:

• **Hardcoded**: agrega un valor fijo al token.  
• **Usermodel Attribute**: toma un atributo del usuario y lo incluye.  
• **Role List**: envía roles según configuración.  
• **Protocol-specific**: depende del protocolo (SAML o OpenID Connect).
          `}
        />

        <Footer text="El tipo de mapper influye en la configuración disponible." />
      </div>
    ),
  },

  // ACTIONS
  {
    selector: '[data-tour="mappers.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Crear nuevo Mapper" />
        <Paragraph
          text={`
Puedes crear un mapper seleccionando:

• Tipo de mapper  
• Claim name  
• Valor fijo o atributo del usuario  
• A qué tokens debe añadirse (Access, ID, UserInfo)

Ten presente que algunas opciones dependen del protocolo.
          `}
        />
        <Footer text="Elige bien el tipo de mapper según lo que desees transmitir." />
      </div>
    ),
  },

  // TABLE
  {
    selector: '[data-tour="mappers.table"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Listado de Mappers" />
        <Paragraph
          text={`
Aquí puedes ver todos los mappers existentes para este Client o Client Scope.
Cada fila muestra el nombre, la descripción y el tipo de mapper.
          `}
        />
      </div>
    ),
  },

  // TABLE ACTIONS
  {
    selector: '[data-tour="mappers.table.actions"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Acciones por Mapper" />

        <Paragraph
          text={`
• **Editar**: permite modificar el tipo, claim y configuración.  
• **Eliminar**: borra definitivamente el mapper.  
• **Ver configuración**: según tu interfaz, puede mostrar detalles adicionales.

Ten en cuenta que algunos mappers vienen preconfigurados por el sistema
y pueden tener restricciones.
          `}
        />

        <Footer text="Usa estas acciones para ajustar cómo se construyen los tokens." />
      </div>
    ),
  },

  // PAGINATION
  {
    selector: '[data-tour="mappers.table.pagination"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Paginación" />
        <Paragraph text="Navega entre páginas para revisar todos los mappers asociados." />
        <Footer text="Listo. Ya conoces la sección de Mappers." />
      </div>
    ),
  },
];
```




### credenciales

```
<h1 data-tour="credentials.title"></h1>

<div data-tour="credentials.secret"></div>

<button data-tour="credentials.secret.regenerate"></button>

<div data-tour="credentials.flows"></div>

<button data-tour="credentials.update"></button>





import { StepType } from "@reactour/tour";
import { Title } from "@/components/tour/Title";
import { Paragraph } from "@/components/tour/Paragraph";
import { Footer } from "@/components/tour/Footer";
import { EMOJIS } from "@/constants/emojis";

export const credentialsSteps: StepType[] = [
  // INTRO
  {
    selector: "body",
    content: () => (
      <div>
        <Title text={`${EMOJIS.lock} Credenciales del Cliente`} />
        <Paragraph
          text={`
Aquí puedes administrar la información sensible relacionada a la autenticación
del cliente, como su Client Secret y los flujos de autenticación permitidos.
          `}
        />
        <Footer text="Vamos a ver cada parte en detalle." />
      </div>
    ),
  },

  // TITLE
  {
    selector: '[data-tour="credentials.title"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Sección de Credenciales" />
        <Paragraph
          text={`
Cada cliente tiene credenciales únicas que permiten validar su identidad
al interactuar con otros servicios. Aquí puedes consultarlas y administrarlas.
          `}
        />
      </div>
    ),
  },

  // CLIENT SECRET
  {
    selector: '[data-tour="credentials.secret"]',
    position: "right",
    content: () => (
      <div>
        <Title text="Client Secret" />
        <Paragraph
          text={`
El *Client Secret* es la clave privada que autentica al cliente
cuando se comunica mediante flujos confidenciales.
Tenla presente: es información sensible y debe mantenerse segura.
          `}
        />
        <Footer text="Puedes ocultarla o visualizarla según lo necesites." />
      </div>
    ),
  },

  // REGENERATE
  {
    selector: '[data-tour="credentials.secret.regenerate"]',
    position: "bottom",
    content: () => (
      <div>
        <Title text="Regenerar Secret" />
        <Paragraph
          text={`
Este botón genera un nuevo Client Secret.
Es útil si crees que la clave fue comprometida o necesitas rotarla por seguridad.

⚠ Recuerda: al regenerar, integraciones externas dejarán de funcionar
hasta actualizar la clave en sus configuraciones.
          `}
        />
        <Footer text="Úsalo solo cuando sea necesario." />
      </div>
    ),
  },

  // FLOWS
  {
    selector: '[data-tour="credentials.flows"]',
    position: "left",
    content: () => (
      <div>
        <Title text="Flujos de Autenticación" />
        <Paragraph
          text={`
Aquí puedes habilitar o deshabilitar los flujos permitidos para este cliente.

Cada flujo representa una forma distinta de cómo la aplicación puede obtener tokens:
          
• **Standard Flow** – Usado por aplicaciones web.  
• **Implicit Flow** – Para apps SPA (legacy).  
• **Direct Access Grants** – Permite que el usuario envíe credenciales directamente.  
• **Service Account** – Credenciales para integración servidor-servidor.  
• **Authorization Services** – Activa control de permisos avanzado.  
• **Public Client** – El cliente no tiene secret; útil para SPAs o apps móviles.

Dependiendo de la arquitectura, algunos flujos pueden no ser recomendados.
          `}
        />
        <Footer text="Activa solo los flujos que tu aplicación necesite." />
      </div>
    ),
  },

  // UPDATE BUTTON
  {
    selector: '[data-tour="credentials.update"]',
    position: "top",
    content: () => (
      <div>
        <Title text="Guardar Cambios" />
        <Paragraph
          text={`
Una vez configurados los flujos, debes aplicar los cambios desde este botón.
De lo contrario, las nuevas reglas no tendrán efecto.
          `}
        />
        <Footer text="¡Eso es todo! Ya conoces las credenciales de un cliente." />
      </div>
    ),
  },
];
```