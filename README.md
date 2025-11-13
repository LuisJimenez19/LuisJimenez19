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


const validNameRegex = /^[A-Za-zÁÉÍÓÚÜÑáéíóúüñ]+(?: [A-Za-zÁÉÍÓÚÜÑáéíóúüñ]+)*$/;

"withoutSpecialChars": /^[A-Za-zÁÉÍÓÚÜÑáéíóúüñ\s]+$/,


    if (attribute != null && value != null) {
        users = users.stream()
            .filter(u -> {
                switch (attribute) {
                    case "username":
                        return u.getUsername() != null && u.getUsername().toLowerCase().contains(value.toLowerCase());
                    case "email":
                        return u.getEmail() != null && u.getEmail().toLowerCase().contains(value.toLowerCase());
                    default:
                        return false;
                }
            })
            .toList();
    }



español:

{
  "required": "El campo {{field}} es obligatorio.",
  "min": "El campo {{field}} debe tener al menos {{count}} caracteres.",
  "max": "El campo {{field}} no puede superar los {{count}} caracteres.",
  "email": "Ingrese un correo electrónico válido.",
  "invalid_format": "El campo {{field}} tiene un formato inválido.",
  "invalid_number": "El campo {{field}} debe ser un número válido.",
  "invalid_url": "El campo {{field}} debe ser una URL válida.",
  "pattern": "El campo {{field}} no cumple con el formato requerido.",
  "unique": "Ya existe un registro con este {{field}}.",
  "not_allowed_chars": "El campo {{field}} no debe contener caracteres especiales.",
  "no_spaces": "El campo {{field}} no debe contener espacios.",
  "no_numbers": "El campo {{field}} no debe contener números.",
  "select_option": "Debe seleccionar al menos una opción.",
  "mismatch": "Los valores de {{field}} no coinciden.",
  "boolean": "El campo {{field}} debe ser verdadero o falso.",
  "min_value": "El valor de {{field}} debe ser mayor o igual a {{min}}.",
  "max_value": "El valor de {{field}} debe ser menor o igual a {{max}}.",
  "length": "El campo {{field}} debe tener exactamente {{count}} caracteres.",
  "date": "El campo {{field}} debe ser una fecha válida.",
  "future_date": "El campo {{field}} debe ser una fecha futura.",
  "past_date": "El campo {{field}} debe ser una fecha pasada."
}



inglés 

{
  "required": "The {{field}} field is required.",
  "min": "The {{field}} must have at least {{count}} characters.",
  "max": "The {{field}} cannot exceed {{count}} characters.",
  "email": "Please enter a valid email address.",
  "invalid_format": "The {{field}} has an invalid format.",
  "invalid_number": "The {{field}} must be a valid number.",
  "invalid_url": "The {{field}} must be a valid URL.",
  "pattern": "The {{field}} does not match the required pattern.",
  "unique": "A record with this {{field}} already exists.",
  "not_allowed_chars": "The {{field}} must not contain special characters.",
  "no_spaces": "The {{field}} must not contain spaces.",
  "no_numbers": "The {{field}} must not contain numbers.",
  "select_option": "You must select at least one option.",
  "mismatch": "The values for {{field}} do not match.",
  "boolean": "The {{field}} must be true or false.",
  "min_value": "The value of {{field}} must be greater than or equal to {{min}}.",
  "max_value": "The value of {{field}} must be less than or equal to {{max}}.",
  "length": "The {{field}} must have exactly {{count}} characters.",
  "date": "The {{field}} must be a valid date.",
  "future_date": "The {{field}} must be a future date.",
  "past_date": "The {{field}} must be a past date."
}



resources.ts

// src/i18n/resources.ts
type LocaleResources = Record<string, Record<string, any>>;

export const loadResources = (): LocaleResources => {
  const modules = import.meta.glob('./locales/**/*.json', { eager: true });
  const resources: LocaleResources = {};

  for (const path in modules) {
    // Ejemplo: ./locales/es/common.json → [ 'es', 'common' ]
    const parts = path.split('/');
    const lang = parts[2];
    const ns = parts[3].replace('.json', '');

    if (!resources[lang]) resources[lang] = {};
    resources[lang][ns] = (modules[path] as any).default;
  }

  return resources;
};



tour de bienvenida 

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


tour starter


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