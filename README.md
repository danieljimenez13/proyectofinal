# proyectofinal
MARIO DANIEL ARAGONES JIMENEZ /  22-EIIN-1-036
--NOMBRE: MARIO DANIEL ARAGONES JIMENEZ / MATRICULA: 22-EIIN-1-036 
-- Crear la tabla "Empleados"
CREATE TABLE Empleados (
    EmpleadoID INT PRIMARY KEY,
    Nombre VARCHAR(50),
    Cargo VARCHAR(50)
);

-- Crear la tabla "Proyectos"
CREATE TABLE Proyectos (
    ProyectoID INT PRIMARY KEY,
    Nombre VARCHAR(100),
    FechaInicio DATE,
    FechaFin DATE
);

-- Crear la tabla "Asignaciones"
CREATE TABLE Asignaciones (
    AsignacionID INT PRIMARY KEY,
    EmpleadoID INT,
    ProyectoID INT,
    FOREIGN KEY (EmpleadoID) REFERENCES Empleados(EmpleadoID),
    FOREIGN KEY (ProyectoID) REFERENCES Proyectos(ProyectoID)
);

-- Agregar registros a la tabla Empleados
INSERT INTO Empleados (EmpleadoID, Nombre, Puesto)
VALUES
    (1, 'Carlos Méndez', 'Desarrollador'),
    (2, 'Ana Sánchez', 'Diseñadora'),
    (3, 'Luisa Martínez', 'Gerente de Proyecto'),
    (4, 'Pedro Ramirez', 'Analista de Negocios');

-- Agregar registros a la tabla Proyectos
INSERT INTO Proyectos (ProyectoID, NombreProyecto, FechaInicio, FechaFin)
VALUES
    (1, 'Sistema de Gestión Interna', '2023-09-01', '2023-12-15'),
    (2, 'Aplicación Móvil de Clientes', '2023-10-15', '2024-02-28'),
    (3, 'Portal de Ventas en Línea', '2023-11-10', '2024-03-31');

-- Agregar registros a la tabla Asignaciones
INSERT INTO Asignaciones (AsignacionID, EmpleadoID, EmpleadoID)
VALUES
    (1, 1, 1), -- Carlos Méndez asignado al proyecto 1
    (2, 2, 1), -- Ana Sánchez asignada al proyecto 1
    (3, 2, 2), -- Ana Sánchez asignada al proyecto 2
    (4, 3, 3), -- Luisa Martínez asignada al proyecto 3
    (5, 4, 3); -- Pedro Ramirez asignado al proyecto 3





