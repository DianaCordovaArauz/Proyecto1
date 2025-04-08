# Proyecto Volcán Cotopaxi

## Business Understanding: 

### **Antecedentes**

La última erupción del volcán Cotopaxi fue en 1877 y se estima que 60 a
80 millones de metros cúbicos de material se derramaron sobre las
fuentes hídricas principales: el río Pita, el río Cutuchi y el río
Tamboyacu **(Instituto Geofísico de la Escuela Politécnica Nacional,
n.d.)**. Según el Informe Volcánico Especial Cotopaxi, la actividad del
volcán se ha mantenido en un nivel bajo, sin cambios a nivel superficial
como a nivel interno. Este nivel se predice como estable, sin embargo,
el volcán está en constante monitoreo. Los estudios realizados por
diferentes organizaciones como la Escuela Politécnica o el Instituto
Geofísico Nacional no toman en cuenta los impactos socio-económicos de
la posible erupción del Cotopaxi. Es decir, aquellos que afectan la
educación, recuperación económica, e incluso consideran los impactos a
largo plazo como la demora en reconstrucción o los efectos fuera de la
zona inmediata de impact.

### 

### **Factores de riesgo relacionados con la vivienda:**

> **Tipo y material del techo, paredes y piso**
>
> Las viviendas construidas con materiales precarios como paja, zinc,
> madera sin tratamiento o piso de tierra son más propensas a colapsar
> por la acumulación de ceniza volcánica o por movimientos sísmicos
> relacionados. También ofrecen menor protección contra la caída de
> piroclastos y gases.
>
> **Estado físico de la vivienda**
>
> Viviendas con fisuras, techos deteriorados o estructuras debilitadas
> enfrentan mayor riesgo de colapso estructural.
>
> **Acceso a servicios básicos**
>
> La falta de agua potable, saneamiento adecuado y electricidad limita
> la capacidad de resistir y recuperarse tras una erupción.
>
> Por ejemplo, la ceniza puede contaminar fuentes de agua o interrumpir
> la energía.
>
> **Ubicación de la vivienda**
>
> Vivir en zonas cercanas a cauces de lahares, quebradas, o laderas
> inestables incrementa el riesgo geológico directo.
>
> Las viviendas en zonas rurales aisladas pueden enfrentar mayor
> dificultad de evacuación.
>
> **Tenencia de la vivienda**
>
> Las personas que arriendan o viven en ocupaciones informales suelen
> tener menor capacidad de adaptación y acceso a ayudas públicas
> post-desastre.

### **Factores de Riesgo Relacionados con el Hogar**

> **Tamaño y composición del hogar**
>
> Hogares numerosos o con alta proporción de personas dependientes
> (niños, personas mayores, personas con discapacidad) enfrentan más
> dificultades para movilizarse o adaptarse rápidamente en caso de
> evacuación.
>
> **Presencia de personas con movilidad limitada**
>
> La evacuación rápida se dificulta cuando hay miembros del hogar que
> requieren cuidados especiales o asistencia.
>
> **Condición socioeconómica**
>
> Hogares con bajos ingresos o sin acceso a recursos materiales y
> tecnológicos (como vehículos, celulares, internet) tienen menor
> capacidad de prepararse, responder y recuperarse.
>
> **Pérdida de miembros del hogar por migración o fallecimiento**
>
> Un hogar afectado por la migración de adultos (fuera del país, por
> ejemplo) o la pérdida reciente de jefes/as de hogar puede tener menor
> capacidad organizativa y financiera.
>
> **Acceso a medios de información**
>
> La falta de televisión, radio o celular puede impedir el acceso a
> alertas tempranas o instrucciones de evacuación.

## Objetivos y Minimum Viable Product

Objetivo General: El proyecrto busca crear una base de datos integral y
actualizada sobre desastres naturales en Quito en los últimos 120 años,
y generar una base de datos nacional de riesgos en Ecuador. Esto
permitirá entender la evolución de la vulnerabilidad social y los
impactos de los desastres, con especial énfasis en los flujos de lodo
del Volcán Cotopaxi, un fenómeno recurrente y potencialmente
catastrófico.

Objetivo Particular: Este proyecto en particular tiene como objetivo
hacer un análisis de vulnerabilidad mediante clustering.

- Cuáles son los indicadores de vulnerabilidad a nivel socio-económico
  que se pueden usar para predecir la vulnerabilidad por zonas ante una
  explosión del volcán Cotopaxi?

> Engregable o Minimum Viable Product: Un sistema que permite
> identificar grupos de hogares con distintos niveles de vulnerabilidad
> habitacional en una provincia específica usando clustering no
> supervisado. El resultado final debería poder ser cruzado con
> información cartográfica y podrá ser utilizado por instituciones
> públicas, ONGs y organismos internacionales para planificar
> estrategias de mitigación, gestión del riesgo y adaptación climática.

## Data Understanding (Disponibilidad de Datos)

Actualmente, hay diversas fuentes que pueden alimentar este proyecto:

Fuentes disponibles:

1.  Censo de Población y Vivienda 2022 (INEC)

    - Información detallada por zonas censales.

    - Variables sociales, económicas, infraestructura, etc.

    - Útil para vincular exposición y vulnerabilidad.

2.  Registros históricos de desastres (Servicio Nacional de Gestión de
    Riesgos, Municipio de Quito, SNGRE, archivo histórico de prensa)

    - Pueden estar en PDF, reportes escaneados o documentos impresos.

    - Aquí se aplica OCR para digitalizar la información.

3.  Mapas de amenazas volcánicas del IG-EPN (Instituto Geofísico)

    - Modelos de flujo de lodo históricos y proyecciones.

    - Capas geoespaciales compatibles con SIG.

4.  Bases de datos internacionales: EM-DAT, DesInventar, etc.

    - Complemento útil para verificar eventos mayores.

5.  Imágenes satelitales y datos geoespaciales (Google Earth Engine,
    Copernicus, etc.)

    - Para identificar cambios en el territorio y validar zonas de
      riesgo.

Para el proyecto entregable se trabajará con los datos que se encuentran
en el Censo Nacional 2022.

### 

### **Descripción de variables y distribución por importancia:** 

Las variables se elegirán según dos criterios importantes:
vulnerabilidad en términos de vivienda y vulnerabilidad definida según
el acceso a servicios básicos. En ese sentido, las variables que se han
considerado son las siguientes.

**Del dataset "Hogar"**

  -----------------------------------------------------------------------
  **Variable**            **Importancia**
  ----------------------- -----------------------------------------------
  **Provincia**           Media (Ubicación administrativa útil para
                          análisis geográfico pero no directamente para
                          vulnerabilidad)

  **Tipo de vía**         Alta (Indica facilidad de acceso o evacuación
                          en caso de erupción)

  **Tipo de vivienda**    Alta (Condiciones estructurales afectan la
                          protección ante erupciones)

  **Condición de          Alta (Presencia o ausencia de habitantes
  ocupación de vivienda   influye en exposición al riesgo)
  particular**            

  **Condición de          Media (Relevante pero menor frecuencia que
  ocupación de vivienda   vivienda particular)
  colectiva**             

  **Material del techo o  Alta (Techos frágiles aumentan vulnerabilidad a
  cubierta**              ceniza volcánica)

  **Estado del techo o    Alta (Deterioro del techo implica mayor riesgo
  cubierta**              estructural)

  **Material de paredes   Alta (Materiales débiles pueden colapsar ante
  exteriores**            eventos volcánicos)

  **Estado de las paredes Alta (Estado refleja mantenimiento y
  exteriores**            resistencia de la vivienda)

  **Material del piso**   Media (Menor peso estructural que techo o
                          paredes pero refleja condiciones generales)

  **Estado del piso**     Media (Refleja deterioro general, afecta
                          habitabilidad en crisis)

  **Forma de acceso al    Alta (Acceso limitado al agua agrava
  agua**                  vulnerabilidad post-erupción)

  **Fuente del agua**     Alta (Fuentes informales pueden interrumpirse
                          fácilmente en emergencia)

  **Servicio higiénico**  Alta (Falta de saneamiento incrementa riesgo de
                          enfermedades en crisis)

  **Electricidad por red  Alta (Indica estabilidad del suministro
  pública**               eléctrico ante emergencia)

  **Otra fuente de        Media (Refleja nivel de resiliencia energética,
  electricidad**          pero menos común)

  **Eliminación de la     Alta (Método inadecuado indica exposición a
  basura**                contaminación y riesgo en crisis)

  **Número de cuartos**   Media (Tamaño del hogar y hacinamiento inciden
                          en vulnerabilidad)

  **Olla común**          Media (Indica prácticas de cooperación o
                          pobreza, relevante en respuesta comunitaria)

  **Número de hogares**   Media (Hogares múltiples en una vivienda pueden
                          reflejar hacinamiento)

  **Área urbana o rural** Alta (Área rural suele tener menor acceso a
                          servicios y mayor exposición)

  **Cantón**              Media (Ubicación más específica útil para
                          focalización)

  **Identificador de la   Baja (Técnicamente necesaria, no aporta al
  vivienda**              análisis de vulnerabilidad)

  **Total de fallecidos** Media (Puede reflejar impacto reciente o riesgo
                          acumulado)

  **Total de emigrantes** Media (Emigración puede reflejar riesgo
                          percibido o pobreza)

  **Total de personas**   Alta (Tamaño del hogar clave para estimar
                          exposición al riesgo)

  **Condición de          Alta (Simplifica evaluación de exposición en
  ocupación               viviendas)
  (recodificada)**        

  **Número de cuartos     Media (Categoriza mejor el espacio habitable,
  (recodificada)**        relevante en crisis)

  **Déficit               Alta (Síntesis útil del estado estructural de
  habitacional**          la vivienda ante erupción)

  **Registro imputado     Media (Dato técnico útil para entender calidad
  (ocupada sin            del dato, pero no refleja vulnerabilidad)
  personas)**             
  -----------------------------------------------------------------------

### **Del dataset "Vivienda"**

  -----------------------------------------------------------------------
  **Variable**                 **Importancia**
  ---------------------------- ------------------------------------------
  **Provincia**                Media (Ubicación general útil para
                               análisis espacial)

  **Identificador de Cantón**  Media (Ubicación más específica para
                               focalización territorial)

  **Número de vivienda**       Baja (Identificador técnico sin utilidad
                               directa en análisis de vulnerabilidad)

  **Número de hogar**          Baja (Identificador técnico sin utilidad
                               directa en análisis de vulnerabilidad)

  **Número de dormitorios**    Alta (Número de dormitorios refleja
                               condiciones de hacinamiento)

  **Cuarto exclusivo para      Alta (Espacio para cocinar reduce
  cocinar**                    exposición a humo en interiores)

  **Disponibilidad de servicio Alta (Acceso a saneamiento básico es clave
  higiénico**                  para resiliencia en emergencias)

  **Disponibilidad de ducha    Alta (Higiene personal durante crisis
  para bañarse**               volcánicas es esencial para salud)

  **Principal combustible para Alta (Uso de leña o combustibles
  cocinar**                    contaminantes implica mayor
                               vulnerabilidad)

  **Tratamiento del agua para  Alta (Tratamiento del agua refleja
  beber**                      capacidad de adaptación sanitaria)

  **Separa basura orgánica e   Media (Prácticas de gestión de residuos
  inorgánica**                 pueden indicar conciencia ambiental)

  **Separa desperdicios para   Media (Indica costumbres rurales útiles
  animales o plantas**         para análisis de resiliencia alimentaria)

  **Separa reciclables**       Media (Refleja conciencia ambiental y
                               reciclaje, indirectamente ligada a
                               vulnerabilidad)

  **Tiene perros**             Media (Presencia de animales refleja
                               entorno rural, pero no es clave)

  **Número de perros**         Media (Número puede influir en necesidades
                               logísticas, pero no en riesgo estructural)

  **Tiene gatos**              Media (Igual que perros, presencia de
                               gatos no indica mayor vulnerabilidad)

  **Número de gatos**          Media (Número de gatos tiene baja
                               relevancia directa)

  **Tenencia de la vivienda**  Alta (Tipo de tenencia refleja seguridad
                               habitacional y estabilidad)

  **Teléfono convencional**    Baja (Uso en disminución, no aporta mucho
                               a análisis de vulnerabilidad)

  **Teléfono celular**         Alta (Acceso a comunicación clave para
                               evacuación y coordinación)

  **Televisión pagada**        Media (Acceso a medios de comunicación
                               puede reflejar nivel socioeconómico)

  **Internet fijo**            Alta (Acceso a internet indica capacidad
                               de información y alerta)

  **Computadora**              Media (Refleja nivel socioeconómico, menos
                               directo en vulnerabilidad)

  **Refrigeradora**            Alta (Acceso a refrigeración afecta
                               seguridad alimentaria en crisis)

  **Lavadora de ropa**         Media (Indica nivel de vida, pero no
                               crítico para riesgo volcánico)

  **Secadora de ropa**         Baja (No es esencial para análisis de
                               emergencia o riesgo)

  **Horno microondas**         Baja (Electrodoméstico no prioritario para
                               análisis de riesgo)

  **Extractor de olores**      Baja (No incide directamente en capacidad
                               de enfrentar erupción)

  **Automóvil/camioneta**      Media (Movilidad propia puede facilitar
                               evacuación en crisis)

  **Motocicleta**              Media (Movilidad personal útil pero no
                               siempre relevante)

  **Alguien falleció desde     Media (Indica impacto de crisis previas o
  2020**                       actuales)

  **Número de personas         Media (Número de fallecidos refleja
  fallecidas**                 impacto, pero no vulnerabilidad
                               estructural)

  **Alguien emigró desde       Media (Emigración refleja presión
  2010**                       económica o percepción de riesgo)

  **Número de personas         Media (Número refleja intensidad del
  emigrantes**                 fenómeno migratorio)

  **Total de hombres**         Alta (Composición por género clave para
                               análisis de vulnerabilidad diferencial)

  **Total de mujeres**         Alta (Composición por género clave para
                               análisis de vulnerabilidad diferencial)

  **Total de personas**        Alta (Número total de personas define
                               exposición total al riesgo)

  **Persona no mencionada**    Media (Puede indicar subregistro, pero
                               poco impacto directo en modelo)

  **Área urbana o rural**      Alta (Área rural con menor acceso a
                               servicios y mayor exposición física)

  **Cantón (derivada)**        Media (Redundante con identificador
                               anterior, pero útil para localización)

  **Identificador de la        Baja (Identificador técnico sin valor
  vivienda**                   analítico)

  **Identificador del hogar**  Baja (Identificador técnico sin valor
                               analítico)

  **Dormitorios                Media (Recodificación útil para
  (recodificada)**             simplificación del análisis)

  **Registro imputado en       Media (Indica posible sesgo en datos,
  vivienda ocupada sin         importante para validación)
  personas**                   
  -----------------------------------------------------------------------

### 

## Data Preparation (Plan y motivación por pasos)

A continuación se presenta un plan preliminar de preparación de datos.
Aquellos marcados como "No Aplicable" son pasos que no corresponden a
esta parte del proyecto, si no al esfuerzo colectivo del grupo
investigador.

  ------------------------------------------------------------------------
  Paso   Acción                         Motivación
  ------ ------------------------------ ----------------------------------
  1      Limpieza y estructuración del  Tener una base clara de población
         Censo 2022                     y características socioeconómicas
                                        por zona.

  1.1    Creación de indicadores de     Elegir los datos que son
         vulnerabilidad                 relevantes para determinar el
                                        efecto de un desastre natural y la
                                        importancia de cada variable para
                                        predecir su resiliencia y
                                        capacidad de recuperación.

  2      Digitalización de documentos   NO APLICABLE: Extraer datos de
         históricos usando OCR          eventos pasados (fechas,
                                        ubicaciones, tipo de desastre,
                                        daños) que están en PDF o papel.

  3      Normalización y codificación   NO APLICABLE: Establecer
         de eventos                     categorías estandarizadas: tipo de
                                        evento, magnitud, consecuencias.
                                        Facilita análisis temporal y
                                        espacial.

  4      Georreferenciación de datos    NO APLICABLE: Ubicar espacialmente
         históricos                     los eventos usando coordenadas o
                                        sectores administrativos. Permite
                                        cruzar con datos censales.

  5      Integración con capas de       NO APLICABLE: Para identificar
         riesgo (Cotopaxi y otros       poblaciones expuestas en zonas de
         volcanes)                      lahares (flujos de lodo).

  6      Unión de datasets en una base  Fusionar los datos censales,
         maestra                        históricos y geoespaciales en una
                                        estructura coherente.

  7      Análisis exploratorio y        Verificar coherencia temporal y
         limpieza adicional             espacial; tratar valores faltantes
                                        o inconsistentes.

  8      Preparación para modelado o    Dependiendo del objetivo final
         visualización                  (análisis estadístico,
                                        visualización en mapas,
                                        simulaciones).
  ------------------------------------------------------------------------

## EDA

### **EDA para datos por cantón de vivienda y hogar.** 

1.  **Carga de datos**\
    En ambos casos, se comenzaron los procesos cargando los archivos CSV
    (por ejemplo, vivienda_cant.csv y hogar_cant.csv) mediante la
    función pd.read_csv(), especificando el delimitador sep=\';\'.
    Posteriormente, se revisó la estructura de cada DataFrame con
    df.head(), df.info() y df.describe() para asegurar que las columnas
    y sus tipos de datos fueran adecuados.

2.  **Renombrado de columnas**\
    Para cada conjunto de datos, se crearon diccionarios destinados a
    reemplazar los códigos de variables (por ejemplo, I01, H01, etc.)
    por nombres descriptivos (tales como provincia, nro_vivienda,
    nro_hogar). Con estos diccionarios, se aplicó la función
    df.rename(columns=\...) y se obtuvieron:

    - df_renamed, en el caso del dataset de vivienda

    - df_hogar_renamed, en el caso del dataset de hogar

3.  **Inspección y limpieza básicas**\
    Una vez que las columnas fueron renombradas, se exploraron los
    DataFrames para identificar valores nulos y posibles
    inconsistencias. Este paso incluyó verificar si algunas columnas
    requerían conversiones de tipo (por ejemplo, de float a int) o si
    era necesario imputar valores faltantes dependiendo de la estrategia
    de análisis. Los valores faltantes en las exploraciones iniciales no
    tienen una explicación metodológica, sin embargo, la decisión de
    imputar, borrar o usar la moda se pospone por el momento, dado que
    se necesitan más datos para tomar esta decisión.

4.  **Filtrado de datos (opcional)**\
    Para centrarse en el área de interés ---las provincias cercanas al
    volcán Cotopaxi--- se aplicaron filtros a partir de los códigos de
    provincia relevantes (por ejemplo, Tungurahua, Chimborazo, Bolívar,
    Los Ríos, Santo Domingo y Pichincha). Así, se redujo el volumen de
    datos a las zonas específicas que serían analizadas.

5.  **Visualización de distribuciones simples e índices de vulnerabiliad
    que pueden afectar en caso de un desastre natural.**

Se visualizaron datos básicos de vulnerabilidad en cuanto a
infraestructura de la vivienda (estado de paredes, tipo de techo, etc)
así como la cantidad de personas que viven en la vivienda (total
personas, mujeres y hombres). Esto ayudó a identificar las provincias
con mayor vulnerabilidad y presencia de posibles afectados.

6.  **Almacenamiento en SQLite**\
    Una vez ajustados y renombrados, ambos DataFrames finales se
    escribieron en una base de datos SQLite. Se utilizó el método:

df_renamed.to_sql(\'df_renamed_vivienda\', conn, if_exists=\'replace\',
index=False)

df_hogar_renamed.to_sql(\'df_renamed_hogar\', conn,
if_exists=\'replace\', index=False)

De este modo, los datos quedaron disponibles para recuperarlos y
cruzarlos posteriormente desde la misma base de datos, facilitando el
análisis y el modelado. Con estos pasos, se generaron dos tablas limpias
y renombradas ---una relacionada con vivienda y otra con hogar--- que
pueden ser integradas en etapas posteriores de procesamiento.

## Data Wrangling: 

En esta etapa del trabajo, se realizaron tareas de preparación y
depuración de datos provenientes de dos bases censales: una relacionada
con características de la vivienda y otra con características del hogar.
Estas bases fueron almacenadas por separado en archivos de base de datos
SQLite: Cantones.db y Cantones_hogar.db.

1.  **Lectura de datos desde bases SQLite**\
    Se establecieron conexiones con ambas bases de datos mediante la
    librería sqlite3, y se extrajeron las tablas df_renamed_vivienda y
    df_renamed_hogar utilizando consultas SQL a través de
    pandas.read_sql().

2.  **Verificación de columnas clave para la fusión**\
    Se revisaron los nombres de las columnas en ambos conjuntos de datos
    para identificar las llaves necesarias para unirlos. Se determinó
    que las columnas \'provincia\', \'canton_id\', \'id_vivienda\' e
    \'id_hogar\' eran las más adecuadas para realizar la fusión.

3.  **Fusión de las bases de vivienda y hogar**\
    Se ejecutó una unión (merge) de tipo inner entre los dos DataFrames
    para obtener un único conjunto de datos combinado (df_merged) que
    integrara toda la información relevante por vivienda y hogar.

4.  **Exploración y limpieza posterior al merge**\
    Se identificaron y gestionaron columnas con nombres duplicados o
    sufijos (\_x, \_y) tras la fusión. También se verificó que las
    columnas clave estuvieran presentes correctamente y se validó la
    forma final del DataFrame combinado.

5.  **Identificación de variables categóricas para codificación**\
    Se elaboró una lista de variables categóricas presentes en el
    DataFrame resultante, especialmente aquellas con valores discretos
    representando etiquetas (por ejemplo, tipo de vía, tipo de vivienda,
    materiales de construcción, etc.). Estas variables fueron
    seleccionadas para su transformación en variables dummies (one-hot
    encoding), lo cual es esencial para análisis estadísticos o modelado
    predictivo posterior.

6.  **Transformación de variables categóricas**\
    Se convirtieron las columnas seleccionadas a tipo texto (str)
    después de gestionar los valores nulos, con el fin de aplicar
    correctamente la codificación mediante pandas.get_dummies(). Esto
    permite transformar cada categoría en una nueva columna binaria y
    mantener la información sin perder la interpretación de las
    etiquetas originales. Luego, se transformaron las variables
    relativas a la estructura de las viviendas gracias al método
    "one-hot-encoding", que es el apropiado para variables categóricas
    con valores numéricos no relacionales.

7.  **Validación del DataFrame final**\
    Se comprobó la integridad del nuevo DataFrame (df_merged) con las
    transformaciones aplicadas. Esto es solamente uno de los pasos de
    data wrangling que necesitará este dataset y una aproximación a lo
    que requerirá el Proyecto final.

## Feature Engineering

1.  **Cargar datos de una base SQLite**, filtrando solo una provincia
    (provincia = \'5\') y tomando una muestra aleatoria de 1000 filas.

2.  **Eliminación columnas irrelevantes o redundantes**.

Para borrar las variables se usaron tres criterios: redundancia,
irrelevancia y multicolinealidad. Las columnas descartadas incluyen
variables codificadas con sufijos como \_label\_, así como otras
variables categóricas específicas.

En particular:

- Las columnas que comienzan con nro_cuartos_r_label\_,
  nro_emigrantes_label y nro_hogar_label corresponden a versiones
  codificadas o duplicadas de variables ya presentes en su forma
  numérica original (nro_cuartos_r, nro_emigrantes, etc.), por lo que se
  consideraron redundantes.

- Las variables relacionadas con separa_basura y
  fallecidos_ultimos_3_anios_label fueron eliminadas por presentar baja
  relevancia directa en la construcción del índice de vulnerabilidad
  habitacional, además de contener valores que podrían introducir ruido
  en los algoritmos de agrupamiento.

  1.  **Imputación valores faltantes** con KNNImputer: Se usaron los 5
      vecinos más cercanos para imputar los valores faltantes de 5
      variables numéricas. Esta técnica fue seleccionada por su
      capacidad de **preservar la estructura multivariable** de los
      datos, lo cual es especialmente relevante cuando las variables
      están correlacionadas entre sí, como es el caso en contextos de
      análisis social y de condiciones de vida.

  2.  **Eliminación de NaN:** Primero, se procedió a eliminar todas las
      filas que contenían valores nulos en el conjunto de datos original
      (cotopaxi_df). Para ello, se utilizó un método que descarta
      cualquier fila con al menos un valor NaN y, posteriormente, se
      reindexó el DataFrame resultante para mantener una numeración
      continua de los registros. El resultado se almacenó en un nuevo
      DataFrame denominado cotopaxi_df_clean.

  3.  **Creación de variables combinadas e índices:**

## Se creó una nueva variable llamada personas_por_cuarto, calculando la razón entre el número total de personas y el número de cuartos disponibles en la vivienda. Para evitar errores en el cálculo, se reemplazaron los valores infinitos o indefinidos por NaN.

- Con esta variable, se construyó una clasificación del nivel de
  **hacinamiento**, segmentando los valores en tres categorías:
  Aceptable, Moderado y Severo, según los rangos establecidos de
  personas por cuarto. Posteriormente, esta clasificación categórica se
  transformó en una variable numérica ordinal denominada
  hacinamiento_score, donde cada categoría fue mapeada a un valor entre
  0 y 2. Los casos con información insuficiente fueron marcados como
  NaN.

- Luego, se definió un conjunto de variables que representaban
  **condiciones de vulnerabilidad habitacional**, agrupando
  características relacionadas con materiales de construcción precarios
  (en techo, paredes y piso), estados estructurales calificados como
  \"malos\", y situaciones de ocupación inestable de la vivienda. Estas
  variables fueron filtradas para asegurar su existencia en el conjunto
  de datos, y posteriormente se sumaron para generar un **índice de
  vulnerabilidad**, almacenado en la variable vulnerabilidad_vivienda.

## Modeling: 

## Primero, se definió una función destinada a **identificar y eliminar valores atípicos** en el conjunto de datos, utilizando el método del **rango intercuartílico (IQR)**. Para cada una de las columnas especificadas, se calcularon el primer cuartil (Q1) y el tercer cuartil (Q3), y con ello se obtuvo el rango intercuartílico (IQR = Q3 - Q1). A partir de este rango, se establecieron límites inferior y superior (Q1 - 1.5 \* IQR y Q3 + 1.5 \* IQR, respectivamente), y se filtraron aquellas observaciones que se encontraban fuera de este rango, ya que se consideraron potenciales outliers.

## Esta operación se aplicó específicamente a las variables vulnerabilidad_vivienda, personas_por_cuarto y hacinamiento_score, las cuales son clave en la construcción del análisis de vulnerabilidad y no son binarias, como otras en el dataset. 

A continuación, se llevó a cabo una **visualización comparativa del
efecto de la limpieza de outliers** en tres variables clave relacionadas
con la vulnerabilidad: vulnerabilidad_vivienda, personas_por_cuarto y
hacinamiento_score. Para cada variable, se generaron gráficos de caja
(*boxplots*) que permitieron observar su distribución antes y después de
la limpieza. En cada gráfico, se comparó la versión original de la
variable (con posibles valores atípicos) con la versión contenida en el
DataFrame limpio (cotopaxi_df_clean), facilitando así la evaluación
visual del impacto de la eliminación de valores extremos.

MODELOS ELEGIDOS:

**KMEANS**

Justificación: El algoritmo KMeans fue elegido por su eficiencia
computacional y su capacidad para identificar estructuras esféricas en
los datos. Este modelo busca minimizar la varianza intra-cluster,
asignando observaciones al centroide (punto central o promedio de un
grupo de datos) más cercano. Es particularmente adecuado para conjuntos
de datos grandes y cuando se espera que los grupos sean de tamaño
relativamente similar.

HIPERPARÁMETROS:

- Este modelo permite un control directo sobre el número de clusters
  mediante el hiperparámetro n_clusters.

- Un número demasiado bajo puede agrupar hogares con niveles de
  vulnerabilidad muy diferentes en el mismo cluster, perdiendo detalle.

- Un número demasiado alto puede generar clusters muy pequeños o poco
  interpretables, dificultando su uso para el diseño de intervenciones o
  políticas.

- También se puede ajustar init (forma de inicializar los centroides),
  max_iter (número máximo de iteraciones), y random_state para
  garantizar reproducibilidad.

**AGGLOMERATIVE CLUSTERING**

Agglomerative Clustering es un algoritmo jerárquico que no requiere
suposiciones sobre la forma de los clusters y que ofrece una perspectiva
distinta, ya que construye una jerarquía de grupos a partir de la fusión
progresiva de observaciones o clusters cercanos. Este enfoque es útil
para detectar subgrupos más complejos o con formas irregulares, lo cual
puede reflejar mejor la diversidad de situaciones de vulnerabilidad
presentes en la población.

HIPERPARAMETROS

- Este modelo también permite un control directo sobre el número de
  clusters mediante el hiperparámetro n_clusters.

- También se puede ajustar el hiperparámetro linkage (por defecto
  \"ward\"), que determina el criterio para fusionar clusters. Cambiarlo
  a \"single\", \"complete\" o \"average\" puede cambiar las estructuras
  de cluster, haciéndolas más sensibles a la forma de los datos o a la
  presencia de outliers.

  1.  **Escalada de variables**

<!-- -->

- Se seleccionaron tres variables para representar las condiciones de
  vulnerabilidad habitacional: vulnerabilidad_vivienda,
  personas_por_cuarto y hacinamiento_score. Estas variables reflejan
  distintos aspectos estructurales y de hacinamiento que permiten
  caracterizar los hogares desde una perspectiva multidimensional.

- A continuación, se procedió a escalar los datos mediante la técnica de
  estandarización (StandardScaler). Este proceso transforma las
  variables para que tengan una media de 0 y una desviación estándar de
  1, eliminando así las diferencias de magnitud entre ellas.

- La escalación es una etapa fundamental en algoritmos de agrupamiento
  como K-Means, ya que estos métodos utilizan medidas de distancia (como
  la distancia euclidiana) para asignar observaciones a distintos grupos
  o clusters. Sin una escala común, las variables con valores
  numéricamente más grandes podrían dominar el análisis e influir de
  forma desproporcionada en la formación de los clusters. Por tanto, al
  escalar, se asegura que cada variable contribuya de forma equitativa
  al resultado del modelo de clustering.

  1.  Aplicación **de** KMeans con 4 clusters, y guardas el resultado en
      una nueva columna cluster_kmeans.

## Se aplicó el algoritmo de **agrupamiento K-Means** con el objetivo de identificar patrones o perfiles de vulnerabilidad dentro del conjunto de datos. Para ello, se inicializó el modelo con 4 clusters, especificando una semilla aleatoria (random_state=42) para garantizar la reproducibilidad de los resultados.

## El modelo se entrenó sobre los datos previamente escalados (X_scaled), y a cada observación se le asignó un número de cluster correspondiente al grupo al que pertenece, almacenándose este resultado en la nueva columna cluster_kmeans.

1.  **Aplicación de un segundo modelo**

- Además del modelo KMeans, se aplicó también el algoritmo de
  Agrupamiento Jerárquico Aglomerativo (Agglomerative Clustering) para
  comparar los resultados obtenidos. Al igual que en el caso anterior,
  se especificó la formación de 4 grupos (clusters) y se utilizó el
  mismo conjunto de variables previamente escaladas (X_scaled) como
  entrada para el modelo.

- Este método parte de la idea de que cada observación es inicialmente
  su propio grupo y, en sucesivas iteraciones, se agrupan los elementos
  más cercanos entre sí hasta formar los clusters finales. El resultado
  del modelo fue almacenado en una nueva columna del DataFrame llamada
  cluster_agglo.

**ANEXOS:**

  -------------------------------------------------------------------------
                NOMBRE DE LA     CATEGORÍAS\
                VARIABLE         (Código y etiqueta)
  ------------- ---------------- ------------------------------------------
       I01      Provincia        De acuerdo a Clasificador Geográfico
                                 Estadístico

       I02      Identificador de De acuerdo a cartografía censal
                Cantón           

       I10      Número de        De acuerdo a cartografía censal
                vivienda         

       D01      Tipo de vía      1\. Calle\
                                 2. Avenida\
                                 3. Carretera\
                                 4. Pasaje\
                                 5. Callejón\
                                 6. Sendero\
                                 7. Camino\
                                 8. Otro

       V01      Tipo de vivienda 1\. Casa/villa\
                                 2. Departamento en casa o edificio\
                                 3. Cuarto/s en casa de inquilinato.\
                                 4. Mediagua\
                                 5. Rancho\
                                 6. Covacha\
                                 7. Choza\
                                 8. Otra vivienda particular\
                                 9. Hotel, pensión, residencial u hostal\
                                 10. Cuartel militar, policía o bomberos\
                                 11 Centro de privación de libertad/cárcel\
                                 12.Hospital, clínica, etc.\
                                 13. Convento o institución religiosa\
                                 14. Centro de acogida y protección para
                                 niñas/os y adolescentes\
                                 15. Residencia de adultos mayores/Asilo de
                                 ancianos\
                                 16. Internado de estudiantes\
                                 17. Campamento de trabajo\
                                 18. Otra vivienda colectiva\
                                 19. Sin vivienda

      V0201     Condición de     1\. Ocupada con personas presentes\
                ocupación de     2. Ocupada con personas ausentes\
                vivienda         3. De temporada o vacacional\
                particular       4. Desocupada\
                                 5. En construcción

      V0202     Condición de     1\. Con residentes habituales\
                ocupación de     2. Sin residentes habituales
                vivienda         
                colectiva        

       V03      Material         1\. Hormigón (losa, cemento)?\
                predominante del 2. Fibrocemento, asbesto (eternit,
                techo o cubierta eurolit)?\
                                 3. Zinc, aluminio (lámina o plancha
                                 metálica)?\
                                 4.Teja?\
                                 5. Palma, paja u hoja?\
                                 6. Otro material?

       V04      Estado del techo 1\. Bueno?\
                o cubierta       2. Regular?\
                                 3. Malo?

       V05      Material         1\. Hormigón?\
                predominante de  2. Ladrillo o bloque?\
                las paredes      3. Panel prefabricado (yeso, fibrocemento,
                exteriores       etc.)?\
                                 4. Adobe o tapia?\
                                 5. Madera?\
                                 6. Caña revestida o bahareque?\
                                 7. Caña no revestida?\
                                 8. Otro material?

       V06      Estado de las    1\. Bueno?\
                paredes          2. Regular?\
                exteriores       3. Malo?

       V07      Material         1\. Duela, parquet, tablón o piso
                predominante del flotante?\
                piso             2. Cerámica, baldosa, vinil o
                                 porcelanato?\
                                 3. Mármol o marmetón?\
                                 4. Ladrillo o cemento?\
                                 5. Tabla sin tratar?\
                                 6. Caña sin tratar?\
                                 7. Tierra?\
                                 8. Otro material?

       V08      Estado del piso  1\. Bueno?\
                                 2. Regular?\
                                 3. Malo?

       V09      El agua que      1\. Por tubería, dentro de la vivienda?\
                recibe la        2. Por tubería, fuera de la vivienda pero
                vivienda es      dentro del edificio, lote o terreno?\
                                 3. Por tubería, fuera del edificio, lote o
                                 terreno?\
                                 4. No recibe agua por tubería, sino por
                                 otros medios?

       V10      El agua que      1\. Empresa Pública/Municipio?\
                recibe la        2. Juntas de Agua/Organizaciones
                vivienda         comunitarias/GAD parroquial?\
                proviene o es    3. Pozo?\
                suministrada por 4. Carro o tanquero repartidor?\
                                 5. Otras fuentes (río, vertiente, acequia,
                                 canal, grieta o agua lluvia)?

       V11      El servicio      1\. Inodoro o escusado, conectado a red
                higiénico de la  pública de alcantarillado?\
                vivienda es      2. Inodoro o escusado, conectado a pozo
                                 séptico?\
                                 3. Inodoro o escusado, conectado a
                                 biodigestor?\
                                 4. Inodoro o escusado, conectado a pozo
                                 ciego?\
                                 5. Inodoro o escusado, con descarga
                                 directa al mar, río, lago o quebrada?\
                                 6. Letrina?\
                                 7. No tiene

       V12      Disponibilidad   1\. Sí\
                de energía       2. No
                eléctrica por    
                red pública      

       V13      Disponibilidad   1\. Planta eléctrica (generador de luz)?\
                de otra fuente   2. Energía solar (panel fotovoltaico)?\
                de energía       3. Energía eólica (a partir del viento)?\
                eléctrica        4. Otra fuente (desechos vegetales y
                                 animales)?\
                                 5. No dispone

       V14      Eliminación de   1\. Por carro recolector?\
                la basura        2. Por contenedor municipal?\
                                 3. La arroja en terreno baldío?\
                                 4. La quema?\
                                 5. La entierra?\
                                 6. La arroja al río, acequia, canal o
                                 quebrada?\
                                 7. De otra forma?

       V15      Número de        1-20
                cuartos          

       V16      Todas las        1\. Sí\
                personas         2. No
                comparten un     
                mismo gasto para 
                la alimentación  

       V17      Número de        1-9
                hogares          

       AUR      Área urbana o    1\. Área Urbana\
                rural            2. Área Rural

     CANTON     Cantón           De acuerdo a Clasificador Geográfico
                                 Estadístico

     ID_VIV     Identificador de  
                la vivienda      

     TOTFALL    Total de         0-99
                fallecidos de la 
                vivienda         

     TOTEMI     Total de         0-99
                emigrantes de la 
                vivienda         

     TOTPER     Total de         0-9999
                personas de la   
                vivienda         

     V0201R     Condición de     1\. Ocupada\
                ocupación de     2. De temporada o vacacional\
                vivienda         3. Desocupada\
                particular       4. En construcción
                (recodificada)   

      V15R      Número de        1\. Un cuarto\
                cuartos          2. Dos cuartos\
                (recodificada)   3. Tres cuartos\
                                 4. Cuatro cuartos\
                                 5. Cinco cuartos\
                                 6. Seis o más cuartos

     DEF_HAB    Déficit          1\. Dignas o aceptables\
                habitacional     2. Déficit cualitativo (Recuperables)\
                                 3. Déficit cuantitativo (Irrecuperables)

    IMP_VOPA    Registro         1\. Sí\
                imputado en      2. No
                vivienda ocupada 
                con personas     
                ausentes         
  -------------------------------------------------------------------------

DATASET: HOGAR

  ------------------------------------------------------------------------
  **CÓDIGO DE      **NOMBRE DE LA       **CATEGORÍAS\
   VARIABLE**      VARIABLE**           (Código y etiqueta)**
  ------------ --- -------------------- ----------------------------------
      I01          Provincia            De acuerdo a Clasificador
                                        Geográfico Estadístico

      I02          Identificador de     De acuerdo a cartografía censal
                   Cantón               

      I10          Número de vivienda   De acuerdo a cartografía censal

      INH          Número de hogar      00-10

      H01          Número de            0-20
                   dormitorios          

      H02          Cuarto o espacio     1\. Sí\
                   exclusivo para       2. No
                   cocinar              

      H03          Disponibilidad de    1\. De uso exclusivo del hogar\
                   servicio higiénico,  2. Compartido con varios hogares\
                   inodoro o escusado   3. No tiene

      H04          Disponibilidad de    1\. De uso exclusivo del hogar\
                   espacio con          2. Compartido con varios hogares\
                   instalaciones y/o    3. No tiene
                   ducha para bañarse   

      H05          Principal            1\. Gas de tanque o cilindro\
                   combustible o        2. Gas centralizado (por tubería)\
                   energía para cocinar 3. Electricidad\
                                        4. Leña o carbón\
                                        5. Biogás (residuos vegetales y/o
                                        animales, etc.)\
                                        6. Otro (Ej: gasolina, kerex,
                                        diésel, etc.)\
                                        7. Ninguno (no cocina)

      H06          Principalmente, el   1\. La beben, tal como llega al
                   agua que beben los   hogar?\
                   miembros del hogar   2. La compran (agua envasada en
                                        bidón, botella o funda)?\
                                        3. La hierven?\
                                        4. Le ponen cloro?\
                                        5. La filtran (colocan filtros en
                                        el grifo o usan purificadores)?\
                                        6. Realizan otro tratamiento?

     H0701         Acostumbra separar   1\. Sí\
                   la basura en         2. No
                   orgánica e           
                   inorgánica           

     H0702         Acostumbra separar   1\. Sí\
                   desperdicios para    2. No
                   dar a los animales o 
                   plantas              

     H0703         Acostumbra separar   1\. Sí\
                   papel, cartón,       2. No
                   plástico o vidrio    
                   para vender, regalar 
                   o reutilizar         

     H0801         Tiene este hogar     1\. Sí\
                   perros               2. No

     H0801N        Número de perros     1-98

     H0802         Tiene este hogar     1\. Sí\
                   gatos                2. No

     H0802N        Número de gatos      1-98

      H09          Tenencia de la       1\. Propia y totalmente pagada?\
                   vivienda             2. Propia y la está pagando?\
                                        3. Propia (regalada, donada,
                                        heredada o por posesión)?\
                                        4. Arrendada/anticresis?\
                                        5. Prestada o cedida (no paga)?\
                                        6. Por servicios?

     H1001         Dispone de servicio  1\. Sí\
                   de teléfono          2. No
                   convencional         

     H1002         Dispone de servicio  1\. Sí\
                   de teléfono celular  2. No

     H1003         Dispone de servicio  1\. Sí\
                   de televisión pagada 2. No

     H1004         Dispone de servicio  1\. Sí\
                   de internet fijo     2. No

     H1005         Dispone de           1\. Sí\
                   computadora          2. No

     H1006         Dispone de           1\. Sí\
                   refrigeradora        2. No

     H1007         Dispone de máquina   1\. Sí\
                   lavadora de ropa     2. No

     H1008         Dispone de máquina   1\. Sí\
                   secadora de ropa     2. No

     H1009         Dispone de horno     1\. Sí\
                   microondas           2. No

     H1010         Dispone de máquina   1\. Sí\
                   extractora de olores 2. No

     H1011         Dispone de automóvil 1\. Sí\
                   o camioneta para uso 2. No
                   exclusivo            

     H1012         Dispone de           1\. Sí\
                   motocicleta para uso 2. No
                   exclusivo            

      H11          Alguna persona       1\. Sí\
                   falleció en los      2. No\
                   últimos tres años (a 9. Se ignora
                   partir de enero      
                   2020)                

     H1101         Número de personas   1-20
                   fallecidas           

      H12          Alguna persona viajó 1\. Sí\
                   a otro país y        2. No\
                   todavía no regresa   9. Se ignora
                   (a partir de nov.    
                   2010)                

     H1201         Número de personas   1-20
                   emigrantes           

     H1301         Total de hombres en  0-9999
                   el hogar             

     H1302         Total de mujeres en  0-9999
                   el hogar             

     H1303         Total de personas en 1-9999
                   el hogar             

      H15          Existe alguna        1\. Sí\
                   persona que no haya  2. No\
                   sido mencionada en   9. Se ignora
                   el hogar             

      AUR          Área urbana o rural  1\. Área Urbana\
                                        2. Área Rural

     CANTON        Cantón               De acuerdo a Clasificador
                                        Geográfico Estadístico

     ID_VIV        Identificador de la   
                   vivienda             

     ID_HOG        Identificador del     
                   hogar                

      H01R         Número de            0\. Ninguno\
                   dormitorios          1. Un dormitorio\
                   (recodificada)       2. Dos dormitorios\
                                        3. Tres dormitorios\
                                        4. Cuatro dormitorios\
                                        5. Cinco dormitorios\
                                        6. Seis o más dormitorios

    IMP_VOPA       Registro imputado en 1\. Sí\
                   vivienda ocupada con 2. No
                   personas ausentes    

                                        
  ------------------------------------------------------------------------
