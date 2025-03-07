## **1. Funcionalidades Clave del MVP**

### **Gestión de Inventarios con IA:**

- **Carga Inteligente de Inventario:**
    - Los usuarios pueden cargar maquinaria mediante un archivo Excel o introduciendo datos manualmente.
    - La **IA optimiza automáticamente los títulos, descripciones** y categoriza las máquinas según las especificaciones.
- **Categorización Automática:**
    - La IA categoriza automáticamente las maquinarias en categorías relevantes (Ej. Excavadoras, Grúas, etc.), asegurando que el inventario esté bien organizado.

### **Búsqueda Inteligente:**

- **Motor de Búsqueda Avanzado:**
    - Los usuarios pueden buscar maquinaria mediante **filtros avanzados** (por tipo, precio, ubicación) y palabras clave.
    - La IA optimiza los resultados de búsqueda para mostrarlos de manera eficiente, ayudando a los usuarios a encontrar rápidamente lo que buscan.

### **Integración con Marketplaces Externos:**

- **Exportación Automática a Marketplaces:**
    - Los usuarios pueden **exportar su inventario automáticamente** a plataformas como **Mercado Libre**, **Facebook Marketplace**, **Agrofy**, entre otros.
- **Tracking de Fuentes Externas:**
    - La plataforma **monitorea y recoge información** sobre maquinaria disponible en otros marketplaces como Mercado Libre, Facebook Marketplace, Agrofy, y subastas como **Machinery Hunter**, consolidando toda la información en una sola plataforma.

### **Personalización de Catálogos:**

- **Generación de Catálogos Personalizados:**
    - Los usuarios pueden **crear catálogos personalizados** con un diseño simple y fácil de usar, donde pueden añadir su **logo** y modificar detalles básicos como sus colores corporativos.
- **Compartir Catálogos:**
    - Los catálogos generados pueden ser compartidos fácilmente en **WhatsApp**, **redes sociales** y **descargados en formato PDF** con un solo clic.

### **SaaS B2B:**

- **Gestión de Prospectos y Contactos:**
    - Las empresas pueden **organizar y gestionar contactos y prospectos** de forma centralizada dentro de la plataforma y de manera sencilla.
- **Interfaz Profesional:**
    - La plataforma ofrece un **panel de control intuitivo** para gestionar el inventario, ventas, prospectos, y contactos de forma eficiente, adaptado para usuarios no tecnológicos.

### **Interfaz B2B Interconectada con la Interfaz B2C:**

- **Función Interconectada:**
    - Toda la plataforma funciona como una **célula interconectada**, donde los productos que se cargan y se publican en el inventario pasan a estar disponibles (mediante un switch de activación: **público/privado**) dentro del marketplace.
    - **Activación del Producto en Marketplace:**
        - Los productos cargados en el **inventario B2B** se gestionan mediante un **switch** dentro del panel de control:
            - Cuando el switch está en **"Público"**, el producto será **visible en el marketplace** y aparecerá en las plataformas externas como Mercado Libre, Facebook Marketplace, etc.
            - Si el switch está en **"Privado"**, el producto permanecerá solo en el **inventario interno de la empresa**, sin ser visible para el público ni en el marketplace.
    - **Sincronización Automática:**
        - Los productos en **modo público** se sincronizan automáticamente con las plataformas externas, lo que elimina la necesidad de realizar acciones manuales adicionales.
    - **Visibilidad Controlada:**
        - Las empresas pueden controlar de manera sencilla qué productos desean hacer visibles para los consumidores (B2C) y cuáles deben permanecer privados para su gestión interna.
    - **Actualización en Tiempo Real:**
        - Cualquier **cambio realizado en el inventario B2B** (como agregar, actualizar o eliminar productos) se actualiza automáticamente en el marketplace en tiempo real, manteniendo la información consistente en ambas interfaces.
     
----

# Estructura del proyecto Todo Maquinaria dentro de Github

Desglosedetallado y organizado de la estructura completa del proyecto basado en el proyecto de github

---

### **1. Public**

- **lovable-uploads**
    - `b02b5c24-c115-4b33-8a03-f1aee...png`: Imagen cargada en el servidor.
    - `favicon.ico`: Icono del sitio web.
    - `og-image.png`: Imagen para previsualización en redes sociales (Open Graph).
    - `placeholder.svg`: Imagen SVG utilizada como marcador de posición.

---

### **2. Src**

### **Components**

- **Admin**
    - `AdminPanel.tsx`: Componente que gestiona el panel de administración.
    - `PageManager.tsx`: Componente para gestionar las páginas del sistema.
- **Auth**
    - `AuthForm.tsx`: Componente para el formulario de autenticación.
    - `LoginForm.tsx`: Componente para el formulario de inicio de sesión.
    - `RegisterForm.tsx`: Componente para el formulario de registro de usuarios.
    - `SocialButtons.tsx`: Botones para autenticar a través de redes sociales (por ejemplo, Google, Facebook).
- **Catalogo**
    - `ExternalResults.tsx`: Componente para mostrar resultados externos relacionados con el catálogo.
    - `MachineryCard.tsx`: Componente que representa una tarjeta de maquinaria.
    - `MachineryGrid.tsx`: Componente que muestra las maquinarias en una cuadrícula.
    - `SearchFilters.tsx`: Componente que gestiona los filtros de búsqueda para las maquinarias.
- **Dashboard**
    - **Content**
        - `DashboardContent.tsx`: Componente que representa el contenido principal del dashboard.

---

### **3. Supabase**

- **Functions**
    - **batch-machinery-upload**
        - `index.ts`: Función que gestiona la carga en lote de maquinarias.
    - **generate-description**
        - `index.ts`: Función que genera descripciones para las maquinarias.
    - **generate-machinery-pdf**
        - `index.ts`: Función para generar archivos PDF relacionados con maquinarias.
    - **machinery-ai-assistant**
        - **Handlers**
            - `analysis-handler.ts`: Controlador para la parte de análisis de datos de maquinarias.
            - `brand-handler.ts`: Controlador que maneja la información sobre marcas de maquinaria.
            - `category-handler.ts`: Controlador que gestiona las categorías de las maquinarias.
            - `description-handler.ts`: Controlador para la creación y gestión de descripciones.
            - `price-handler.ts`: Controlador para el manejo de precios de las maquinarias.
            - `title-handler.ts`: Controlador que maneja los títulos de las maquinarias.
        - `ai-service.ts`: Servicio relacionado con la inteligencia artificial para la gestión de maquinarias.
        - `config.ts`: Configuración general para la función.
        - `index.ts`: Archivo de entrada principal para esta función.
    - **search-machinery-ai**
        - `index.ts`: Función para gestionar la búsqueda de maquinaria utilizando IA.
    - **search-machinery**
        - `index.ts`: Función para la búsqueda de maquinaria de forma tradicional.
    - **track-market-prices**
        - `index.ts`: Función que realiza el seguimiento de los precios en el mercado de maquinaria.
        - `config.toml`: Archivo de configuración para la función.
        - `.gitignore`: Configuración de archivos que no deben ser versionados.
        - `README.md`: Documentación del proyecto.
        - `bun.lockb`: Archivo de bloqueo para la gestión de dependencias.
        - `components.json`: Archivo que define los componentes utilizados en el proyecto.
        - `eslint.config.js`: Configuración de ESLint para asegurar la calidad del código.
        - `index.html`: Página HTML principal.
        - `package-lock.json`: Archivo de bloqueo de dependencias de Node.js.
        - `package.json`: Archivo de configuración para dependencias y scripts de Node.js.
        - `postcss.config.js`: Configuración de PostCSS para el procesamiento de CSS.
        - `tailwind.config.ts`: Configuración de Tailwind CSS.
        - `tsconfig.app.json`: Configuración de TypeScript para la aplicación.
        - `tsconfig.json`: Configuración de TypeScript.
        - `tsconfig.node.json`: Configuración de TypeScript para entorno Node.
        - `vite.config.ts`: Configuración de Vite como bundler de JavaScript.

---

### **4. Pages**

- **Auth**
    - `callback.tsx`: Componente para manejar el callback de autenticación.
    - `AdminPanel.tsx`: Página para el panel de administración.
    - `BuscarMaquinaria.tsx`: Página para la búsqueda de maquinarias.
    - `BusinessVerification.tsx`: Página para la verificación de negocios.
    - `Catalogo.tsx`: Página que muestra el catálogo de maquinarias.
    - `Dashboard.tsx`: Página principal del dashboard.
    - `EditMachinery.tsx`: Página para editar la maquinaria existente.
    - `GestionLeads.tsx`: Página para la gestión de leads o prospectos.
    - `Index.tsx`: Página de inicio.
    - `Login.tsx`: Página de inicio de sesión.
    - `MachineryDetails.tsx`: Página de detalles de una maquinaria específica.
    - `NotFound.tsx`: Página para el manejo de errores 404 (página no encontrada).
    - `Pricing.tsx`: Página para la visualización de precios.
    - `Register.tsx`: Página para registrar un nuevo usuario.
    - `SubirInventario.tsx`: Página para subir el inventario de maquinarias.
    - `VenderMaquinaria.tsx`: Página para vender maquinarias.

---

### **5. Types**

- `admin.ts`: Tipos relacionados con la administración.
- `editor.ts`: Tipos relacionados con la edición de contenido.

---

### **6. UI**

- `accordion.tsx`: Componente de acordeón para mostrar contenido de forma expandible.
- `alert-dialog.tsx`: Componente de diálogo de alerta.
- `alert.tsx`: Componente para mostrar alertas.
- `avatar.tsx`: Componente para mostrar un avatar de usuario.
- `badge.tsx`: Componente para mostrar insignias o etiquetas.
- `breadcrumb.tsx`: Componente para mostrar la navegación de migas de pan.
- `button.tsx`: Componente de botón.
- `calendar.tsx`: Componente para mostrar un calendario.
- `card.tsx`: Componente para mostrar contenido en formato tarjeta.
- `carousel.tsx`: Componente para crear un carrusel de imágenes o contenido.
- `chart.tsx`: Componente para mostrar gráficos.
- `checkbox.tsx`: Componente de casilla de verificación.
- `collapsible.tsx`: Componente para contenido colapsable.
- `command.tsx`: Componente para ejecutar comandos.
- `context-menu.tsx`: Componente para menú contextual.
- `dialog.tsx`: Componente para mostrar un cuadro de diálogo.
- `drawer.tsx`: Componente para un panel deslizable.
- `dropdown-menu.tsx`: Componente para un menú desplegable.
- `form.tsx`: Componente de formulario.
- `hover-card.tsx`: Componente para mostrar una tarjeta al pasar el ratón.
- `input-otp.tsx`: Componente de entrada de código de un solo uso (OTP).
- `input.tsx`: Componente de entrada de texto.

---

### **7. Registro Final**

- `SuggestNewCategory.tsx`: Componente para sugerir una nueva categoría.
- `SuggestionAlert.tsx`: Componente de alerta de sugerencia.
- `PasoBrandSelection.tsx`: Paso de selección de marca.
- `PasoCategoriaPrincipal.tsx`: Paso de selección de categoría principal.
- `PasoDescripcion.tsx`: Paso de descripción de maquinaria.
- `PasoDetallesBasicos.tsx`: Paso para ingresar detalles básicos.
- `PasoNombreMaquina.tsx`: Paso para ingresar el nombre de la maquinaria.
- `PasoRevision.tsx`: Paso para la revisión de los datos.
- `PasoSubcategorias.tsx`: Paso para seleccionar subcategorías.
- `ProgressBar.tsx`: Barra de progreso para mostrar el avance del proceso.
- **Registro Final**
    - `PricingPlan.tsx`: Página que muestra el plan de precios.
    - `PricingTabsSection.tsx`: Sección de pestañas para los planes de precios.
    - `PublicationSummary.tsx`: Resumen de la publicación.
    - `PublishButton.tsx`: Botón para publicar.
    - `TermsAndConditions.tsx`: Página de términos y condiciones.
    - `constants.ts`: Archivo con constantes de la aplicación.
    - `FormNavigation.tsx`: Componente de navegación en el formulario.
    - `IndicadorPasos.tsx`: Indicador de los pasos en el proceso.
    - `InformacionBasica.tsx`: Página para la información básica.
    - `InventoryForm.tsx`: Formulario para gestionar el inventario.
    - `RegistroFinal.tsx`: Página final de registro de maquinaria.
    - `SubirFotos.tsx`: Página para subir fotos de la maquinaria.

---

### **8. Pasos**

- **Subcategorías**
    - **Components**
        - `CategoryBreadcrumb.tsx`: Componente para la navegación de categorías.
        - `CategoryGroup.tsx`: Componente para agrupar categorías.
        - `EmptyResults.tsx`: Componente que muestra un mensaje cuando no hay resultados.
        - `GridView.tsx`: Componente para mostrar los elementos en una cuadrícula.
        - `ListView.tsx`: Componente para mostrar los elementos en una lista.
        - `NoCategorySelected.tsx`: Componente que muestra un mensaje cuando no se selecciona ninguna categoría.
        - `NoSubcategories.tsx`: Componente que muestra un mensaje cuando no hay subcategorías.
        - `SearchBar.tsx`: Componente para la barra de búsqueda.
        - `SubcategorySelector.tsx`: Componente para seleccionar subcategorías.

---

### **9. Subir Inventario**

- **Components**
    - **Detalles**
        - `LocationInput.tsx`: Componente para ingresar la ubicación.
        - `PriceInput.tsx`: Componente para ingresar el precio.
        - `YearInput.tsx`: Componente para ingresar el año.
        - `InventoryStepContent.tsx`: Componente para mostrar el contenido del paso del inventario.
        - `LoadingCategories.tsx`: Componente que muestra una carga de categorías.
        - `StepContentContainer.tsx`: Contenedor del contenido del paso.
        - `StepNavigation.tsx`: Componente para la navegación entre pasos.
        - `StepRenderer.tsx`: Componente que renderiza los pasos.
    - **Form Fields**
        - `CategorySelector.tsx`: Componente para seleccionar la categoría.
        - `DescriptionField.tsx`: Campo para ingresar una descripción.
        - `FormField.tsx`: Componente genérico para un campo de formulario.
    - **Hooks**
        - **Category**
            - `index.ts`: Archivo de entrada para la lógica relacionada con categorías.
            - `useCategoryAutoSuggest.ts`: Hook para sugerencias automáticas de categorías.
            - `useCategorySelection.ts`: Hook para la selección de categorías.
            - `useCategorySync.ts`: Hook para sincronizar categorías.
            - `useCategoryUtils.ts`: Utilidades relacionadas con categorías.
        - **Navigation**
            - `useStepNavigation.ts`: Hook para la navegación entre pasos.

---

### **10. Editor**

- **Blocks**
    - `CTABlock.tsx`: Componente de bloque para llamada a la acción (CTA).
    - `FeaturesBlock.tsx`: Componente de bloque para características.
    - `HeroBlock.tsx`: Componente de bloque para la sección hero.
    - `ImageBlock.tsx`: Componente de bloque para imágenes.
    - `PricingBlock.tsx`: Componente de bloque para precios.
    - `TextBlock.tsx`: Componente de bloque para texto.
    - `BlockControls.tsx`: Controles para el bloque.
    - `BlockEditor.tsx`: Editor para los bloques.
    - `BlockRenderer.tsx`: Renderizador de bloques.
- **Home**
    - `CTASection.tsx`: Componente para la sección de llamada a la acción.
    - `FeaturedMachinery.tsx`: Componente para mostrar maquinaria destacada.
    - `FeaturesSection.tsx`: Componente para la sección de características.
    - `Header.tsx`: Componente para el encabezado.
    - `HeroSection.tsx`: Componente para la sección hero.
    - `ContactForm.tsx`: Componente para el formulario de contacto.
    - `DetailsContent.tsx`: Componente para mostrar contenido de detalles.
    - `DetailsHeader.tsx`: Encabezado para los detalles.
    - `DetailsSidebar.tsx`: Barra lateral de detalles.
    - `ImageGallery.tsx`: Galería de imágenes.
    - `SpecificationsList.tsx`: Componente para la lista de especificaciones.

---

### **11. Settings**

- **Components**
    - `FooterSettings.tsx`: Configuración para el pie de página.
    - `HeaderSettings.tsx`: Configuración para el encabezado.
    - `PDFPreviewSection.tsx`: Componente para la sección de vista previa de PDF.
    - `PDFSettingsForm.tsx`: Formulario para la configuración de PDF.
    - `ColorSettings.tsx`: Configuración de colores.
    - `LogoUploader.tsx`: Componente para cargar un logo.
    - `PDFPreview.tsx`: Vista previa del PDF.
    - `PDFTemplateSettings.tsx`: Configuración de plantillas para el PDF.
    - `TemplateSelector.tsx`: Selector de plantillas.
    - `types.ts`: Tipos utilizados en los ajustes.
    - **Admin**
        - `AdminEditModeToggle.tsx`: Componente para alternar el modo de edición del administrador.
        - `DashboardHeader.tsx`: Componente para el encabezado del dashboard.
        - `DashboardNav.tsx`: Componente para la navegación del dashboard.
        - `MachineryList.tsx`: Componente para listar las maquinarias.
        - `MessagesTab.tsx`: Pestaña de mensajes en el dashboard.
        - `MetricsTab.tsx`: Pestaña de métricas en el dashboard.
        - `PDFCustomizer.tsx`: Personalizador de PDFs.
        - `PlaceholderTabs.tsx`: Pestañas de marcador de posición.
        - `StatCards.tsx`: Tarjetas de estadísticas.
        - `useDashboard.ts`: Hook para manejar el dashboard.

---

### **12. Dashboard**

- **Content**
    - `DashboardContent.tsx`: Componente para mostrar el contenido del dashboard.
- **Leads**
    - `LeadList.tsx`: Componente para listar los leads.
    - `LeadsTab.tsx`: Pestaña para manejar los leads.
- **Machinery**
    - `CardActions.tsx`: Componente para las acciones de las tarjetas de maquinaria.
    - `CardHeader.tsx`: Encabezado de la tarjeta de maquinaria.
    - `EmptyState.tsx`: Componente que muestra un estado vacío.
    - `LoadingState.tsx`: Componente para el estado de carga.
    - `MachineryCard.tsx`: Tarjeta para mostrar la información de la maquinaria.
    - `MachineryContent.tsx`: Contenido principal de la maquinaria.
    - `MachineryToolbar.tsx`: Barra de herramientas de la maquinaria.
    - `PreviewPanel.tsx`: Panel de vista previa.
    - `ShareDialog.tsx`: Componente para compartir maquinaria.
- **Metrics**
    - `MessagesChart.tsx`: Componente para mostrar un gráfico de mensajes.
    - `TimeRangeSelector.tsx`: Selector de rango de tiempo.
    - `TopMachinesChart.tsx`: Gráfico para mostrar las mejores máquinas.
    - `ViewsChart.tsx`: Gráfico de vistas.
    - `useMetricsData.ts`: Hook para manejar los datos de métricas.
- **Navigation**
    - `DashboardTabs.tsx`: Componente para las pestañas del dashboard.
