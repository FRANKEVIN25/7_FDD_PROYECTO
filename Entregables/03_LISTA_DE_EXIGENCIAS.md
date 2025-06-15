# "Año de la recuperación y consolidación de la economía peruana"

## UNIVERSIDAD PERUANA CAYETANO HEREDIA
### Facultad de Ciencias e Ingeniería

---

# Fundamentos de Diseño

## LISTA DE EXIGENCIAS

---

**PROYECTO:** Diseño de sensor portátil para medición de emisiones vehiculares en tiempo real  
**CLIENTE:** UNIVERSIDAD PERUANA CAYETANO HEREDIA  
**Páginas:** 5  
**Edición:** Rev. 3  
**Fecha:** 14/06/2025  

**Elaborado por:**
- Nathalia Silvana Robledo Cerna
- Frank Jauregui Bendezu
- Jonathan
- Antony

---

## Tabla de Exigencias

| Fecha | D/E | Descripción | Responsable |
|-------|-----|-------------|-------------|
| **14/06/25** | **E** | **Función Principal:** Medir en tiempo real las concentraciones de contaminantes generados por motores de combustión interna directamente desde el tubo de escape, específicamente:<br>• Monóxido de carbono (CO): 0-10% con precisión ±0.1%<br>• Dióxido de carbono (CO₂): 0-20% con precisión ±0.5%<br>• Óxidos de nitrógeno (NOx): 0-5000 ppm con precisión ±50 ppm<br>• Hidrocarburos (HC): 0-2000 ppm con precisión ±20 ppm<br><br>El sistema debe proporcionar lecturas continuas con una frecuencia de muestreo mínima de 1 Hz. | Nathalia Silvana Robledo Cerna |
| **14/06/25** | **E** | **Geometría:** El sensor estará contenido dentro de una caja compacta con las siguientes especificaciones:<br><br>**→ Dimensiones de la caja: 17 cm (largo) × 6 cm (ancho) × 6 cm (alto)**<br><br>• Material de la carcasa: ABS o PLA (impresión 3D) con espesor mínimo de 3 mm<br>• Peso máximo del conjunto completo: 1.2 kg<br>• Tubo de conexión al escape:<br>&nbsp;&nbsp;- Longitud: 25-30 cm (ajustable)<br>&nbsp;&nbsp;- Diámetro interno: 4-5 cm (adaptable a escapes estándar)<br>&nbsp;&nbsp;- Material: Silicona resistente a altas temperaturas (hasta 200°C)<br>• Sistema de acople rápido tipo abrazadera para conexión sin herramientas<br>• Ventilaciones laterales para disipación térmica (mínimo 4 rejillas de 2×3 cm)<br>• Compartimento interno aislado térmicamente para electrónica sensible | Frank Jauregui Bendezu |
| **14/06/25** | **E** | **Energía:** Sistema de alimentación dual con las siguientes características:<br>• Alimentación principal: Batería recargable Li-Po 3S (11.1V, 2200mAh mínimo)<br>• Alimentación auxiliar: Conexión USB-C para carga y operación simultánea<br>• Consumo energético:<br>&nbsp;&nbsp;- Modo normal: 4-6 W<br>&nbsp;&nbsp;- Modo limpieza (con calefactor): hasta 12 W<br>&nbsp;&nbsp;- Modo standby: < 0.5 W<br>• Autonomía mínima: 4 horas en operación continua<br>• Indicador LED de nivel de batería (4 niveles)<br>• Protección contra sobrecarga y descarga profunda | Antony |
| **14/06/25** | **E** | **Programación:** Sistema basado en microcontrolador con las siguientes especificaciones:<br>• Plataforma: Arduino Mega 2560 o compatible<br>• Lenguaje: C++ con librerías optimizadas para sensores de gases<br>• Funcionalidades del software:<br>&nbsp;&nbsp;- Adquisición y procesamiento de datos en tiempo real<br>&nbsp;&nbsp;- Algoritmos de compensación por temperatura y presión<br>&nbsp;&nbsp;- Detección automática de condiciones de saturación del sensor<br>&nbsp;&nbsp;- Ciclos de autolimpieza programables (cada 30 minutos de uso)<br>&nbsp;&nbsp;- Almacenamiento de datos en tarjeta SD (formato CSV)<br>&nbsp;&nbsp;- Comunicación Bluetooth 5.0 para transmisión de datos<br>&nbsp;&nbsp;- Interfaz de calibración mediante comandos AT<br>• Memoria para almacenar mínimo 1000 mediciones | Frank Jauregui Bendezu |
| **14/06/25** | **E** | **Materiales y Sensores:** Componentes específicos para la medición precisa:<br>• Sensor multigás MQ-135 o equivalente para detección preliminar<br>• Sensor NDIR (Non-Dispersive Infrared) para CO₂ de alta precisión<br>• Sensor electroquímico para CO (vida útil mínima: 2 años)<br>• Sensor de NOx tipo semiconductor con calefactor integrado<br>• Filtro de partículas reemplazable (malla de acero inoxidable 100 mesh)<br>• Trampa de condensados con drenaje manual<br>• Aislamiento térmico: lámina de mica o fibra cerámica (2 mm espesor)<br>• Todos los materiales deben soportar temperaturas de hasta 150°C | Nathalia Silvana Robledo Cerna |
| **14/06/25** | **E** | **Control y Calibración:** Sistema de control de calidad integrado:<br>• Autocalibración al encendido con aire ambiente (baseline)<br>• Calibración manual con gases patrón certificados<br>• Compensación automática por:<br>&nbsp;&nbsp;- Temperatura ambiente: -10°C a +50°C<br>&nbsp;&nbsp;- Humedad relativa: 10% a 90% sin condensación<br>&nbsp;&nbsp;- Presión atmosférica: 500-1100 mbar<br>• Alarmas configurables para cada gas según normativa peruana<br>• Registro de eventos de calibración con fecha y hora<br>• Verificación automática de integridad de sensores cada 24 horas | Nathalia Silvana Robledo Cerna |
| **14/06/25** | **E** | **Fabricación:** Proceso de manufactura optimizado:<br>• Carcasa principal: Impresión 3D en PLA+ o ABS (resistente a UV)<br>• Componentes electrónicos: Montaje en PCB de doble cara con soldadura libre de plomo<br>• Ensamblaje modular con conectores tipo JST para fácil mantenimiento<br>• Sellado IP54 para protección contra polvo y salpicaduras<br>• Acabado con pintura epóxica resistente a hidrocarburos<br>• Control de calidad según normas:<br>&nbsp;&nbsp;- Ley N° 30224 - Sistema Nacional para la Calidad<br>&nbsp;&nbsp;- NTP-ISO/IEC 17025 para laboratorios de ensayo<br>• Manual de usuario y mantenimiento en español | Antony |
| **14/06/25** | **E** | **Emisión de Resultados:** Sistema integral de visualización y comunicación:<br>• Display OLED 0.96" integrado en el dispositivo:<br>&nbsp;&nbsp;- Visualización simultánea de los 4 gases<br>&nbsp;&nbsp;- Gráficos de tendencia en tiempo real<br>&nbsp;&nbsp;- Menú de configuración intuitivo<br>• Aplicación móvil (Android/iOS) con funciones:<br>&nbsp;&nbsp;- Dashboard en tiempo real con gráficas dinámicas<br>&nbsp;&nbsp;- Histórico de mediciones con exportación a Excel/PDF<br>&nbsp;&nbsp;- Comparación con LMP según D.S. N° 010-2017-MINAM<br>&nbsp;&nbsp;- Generación automática de informes técnicos<br>&nbsp;&nbsp;- Geolocalización de mediciones<br>• Sistema de indicación visual y sonora:<br>&nbsp;&nbsp;- LED RGB de alta intensidad (visible a plena luz del día)<br>&nbsp;&nbsp;- Verde: Emisiones < 70% del LMP<br>&nbsp;&nbsp;- Amarillo: Emisiones entre 70-100% del LMP<br>&nbsp;&nbsp;- Rojo: Emisiones > 100% del LMP<br>&nbsp;&nbsp;- Alarma sonora configurable (70-90 dB) | Antony |
| **14/06/25** | **E** | **Portabilidad:** Diseño ergonómico para uso en campo:<br><br>**→ Dimensiones compactas: 17 × 6 × 6 cm**<br><br>• Peso total del sistema: < 1.0 kg (incluyendo batería)<br>• Asa de transporte integrada con grip antideslizante<br>• Maletín de transporte rígido incluido con:<br>&nbsp;&nbsp;- Compartimentos para accesorios<br>&nbsp;&nbsp;- Espuma protectora personalizada<br>&nbsp;&nbsp;- Dimensiones del maletín: 30 × 25 × 10 cm<br>• Correa ajustable para uso hands-free<br>• Base magnética para fijación temporal en superficies metálicas | Jonathan |
| **14/06/25** | **E** | **Mantenimiento:** Sistema diseñado para mantenimiento preventivo y correctivo:<br>• Mantenimiento preventivo:<br>&nbsp;&nbsp;- Limpieza de filtros: cada 50 horas de uso<br>&nbsp;&nbsp;- Calibración de sensores: mensual<br>&nbsp;&nbsp;- Verificación de sellos: trimestral<br>&nbsp;&nbsp;- Actualización de firmware: según disponibilidad<br>• Mantenimiento correctivo:<br>&nbsp;&nbsp;- Sensores reemplazables individualmente<br>&nbsp;&nbsp;- PCB modular con diagnóstico de fallas integrado<br>&nbsp;&nbsp;- Códigos de error específicos en display<br>&nbsp;&nbsp;- Kit de repuestos básicos incluido<br>• Vida útil esperada: 5 años con mantenimiento adecuado<br>• Garantía: 1 año para componentes electrónicos | Frank Jauregui Bendezu |
| **14/06/25** | **E** | **Costos:** Presupuesto detallado y optimizado:<br>• Costo objetivo total: S/. 250-350<br>• Desglose estimado:<br>&nbsp;&nbsp;- Sensores de gases: S/. 120-150<br>&nbsp;&nbsp;- Arduino Mega y componentes electrónicos: S/. 60-80<br>&nbsp;&nbsp;- Carcasa y materiales de fabricación: S/. 30-40<br>&nbsp;&nbsp;- Batería y sistema de carga: S/. 25-35<br>&nbsp;&nbsp;- Display OLED y LEDs: S/. 15-25<br>&nbsp;&nbsp;- Accesorios y conectores: S/. 10-20<br>• Costo de mantenimiento anual estimado: S/. 50-80<br>• ROI esperado: 6-8 meses en uso comercial | Frank Jauregui Bendezu |
| **14/06/25** | **E** | **Plazos:** Cronograma detallado del proyecto:<br>• **Fase 1 - Diseño conceptual (15-31 mayo):**<br>&nbsp;&nbsp;- Investigación de mercado y normativas<br>&nbsp;&nbsp;- Especificaciones técnicas finales<br>&nbsp;&nbsp;- Diseño CAD preliminar<br>• **Fase 2 - Desarrollo (1-15 junio):**<br>&nbsp;&nbsp;- Programación del firmware<br>&nbsp;&nbsp;- Diseño de PCB<br>&nbsp;&nbsp;- Impresión 3D de prototipos<br>• **Fase 3 - Integración (16-25 junio):**<br>&nbsp;&nbsp;- Ensamblaje del prototipo<br>&nbsp;&nbsp;- Pruebas de laboratorio<br>&nbsp;&nbsp;- Calibración inicial<br>• **Fase 4 - Validación (26 junio - 10 julio):**<br>&nbsp;&nbsp;- Pruebas de campo en vehículos reales<br>&nbsp;&nbsp;- Ajustes finales<br>&nbsp;&nbsp;- Documentación técnica<br>&nbsp;&nbsp;- Presentación final<br>• Gestión del proyecto: GitHub con commits diarios | Nathalia Silvana Robledo Cerna |
| **14/06/25** | **D** | **Certificaciones y Normativas (Deseable):** Cumplimiento con estándares nacionales e internacionales:<br>• Certificación CE para compatibilidad electromagnética<br>• Cumplimiento con D.S. N° 010-2017-MINAM (LMP para vehículos)<br>• Certificación IP54 para protección ambiental<br>• Conformidad con NTP 900.034:2018 para equipos de medición<br>• Registro en INDECOPI como equipo de medición | Equipo completo |
| **14/06/25** | **D** | **Funciones Adicionales (Deseables):** Características avanzadas para versiones futuras:<br>• Medición de material particulado (PM2.5 y PM10)<br>• Análisis de opacidad para motores diésel<br>• Conexión 4G/LTE para transmisión remota de datos<br>• Integración con sistemas de gestión de flotas<br>• Modo de diagnóstico OBD-II complementario<br>• Cámara térmica para detección de puntos calientes | Equipo completo |

---

## Notas:

- **E = Exigencia** (requisito obligatorio)
- **D = Deseo** (requisito opcional)
- Todos los requisitos marcados con "E" deben cumplirse para la aprobación del proyecto
- Los requisitos "D" serán implementados según disponibilidad de recursos y tiempo
- Esta lista de exigencias está sujeta a revisiones según el avance del proyecto

---

## Firmas de Aprobación:

|                    |                      |                |                        |
|--------------------|----------------------|----------------|------------------------|
| __________________ | ____________________ | ______________ | ______________________ |
| Jefe de Proyecto   | Supervisor Técnico   | Cliente        | Fecha de Aprobación    |

---

*Documento generado el 14 de junio de 2025*  
*Universidad Peruana Cayetano Heredia - Facultad de Ciencias e Ingeniería*
