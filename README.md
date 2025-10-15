** pdg2025-fcen-uba-TP-3 **
** 2025 Procesamiento de Geometría Digital (Digital Geometry Processing) **

Trabajo Practico 3

Los archivos están organizados como en el trabajo practico 2 y el
proceso de compilación es el mismo.

Antes de compilar la aplicación por primera vez, edite el archivo
src/gui/GuiStrings.hpp o cópielo del trabajo practico 1.

Debe implementar los siguientes métodos nuevos, que se han añadido a las
clases HalfEdges y PolygonMesh:

  int     HalfEdges::getFace(const int iC) const;
  int     HalfEdges::getFaceSize(const int iC) const;
  bool    HalfEdges::isOriented(const int iC) const;
  int     HalfEdges::getNumberOfFacesEdge(const int iE) const;

  bool    HalfEdges::hasBoundaryEdges() const;
  bool    HalfEdges::hasRegularEdges() const;
  bool    HalfEdges::hasSingularEdges() const;

  bool    HalfEdges::isBoundaryEdge(const int iE) const;
  bool    HalfEdges::isRegularEdge(const int iE) const;
  bool    HalfEdges::isSingularEdge(const int iE) const;

  int     PolygonMesh::computeConnectedComponentsPrimal
          (vector<int>& faceLabel) const;
  int     PolygonMesh::computeConnectedComponentsDual
          (vector<int>& faceLabel) const;

  bool    PolygonMesh::isOriented() const;
  bool    PolygonMesh::isOrientable() const; 
  int     PolygonMesh::orient(vector<int>& ccIndex, vector<bool>& invert_face);

  int     PolygonMesh::numberOfIsolatedVertices();
  void    PolygonMesh::getIsolatedVertices(vector<int>& isolated_vertex);
  bool    PolygonMesh::removeIsolatedVertices
          (vector<int>& coordMap, vector<int>& coordIndexOut);

  void    PolygonMesh::cutThroughSingularVertices
          (vector<int>& vIndexMap, vector<int>& coordIndexOut);

  void    PolygonMesh::convertToManifold
          (vector<int>& vIndexMap, vector<int>& coordIndexOut);

y completar el programa de prueba de línea de comandos dgpTest3.

Debe fusionar el código de la Tarea 2 de las clases Faces, HalfEdges y
PolygonMesh con los nuevos archivos proporcionados. Las clases Edges
y Graph estan implementadas con cambios menores.

Se han realizado varios cambios en otras clases y se han añadido
nuevas clases al repositorio. No fusione archivos antiguos, ya que la
aplicación podría no compilar.

Se incluyen instrucciones adicionales como comentarios en los archivos
fuente y se discutirán en clase.

Los nuevos archivos de prueba se subirán a Campus como un archivo zip.

Entrega:

a) Localice y elimine los archivos temporales creados por su editor.
b) Elimine el contenido de los subdirectorios superiores bin y build.
c) Elimine el archivo qt/DGP2025-A3.pro.user creado por QtCreator.
d) Elimine el directorio principal build creado por QtCreator.
e) Confirme todos los cambios a intervalos regulares y en los hitos.
f) Publique sus confirmaciones en su repositorio de GitHub.
g) Siga las instrucciones de entrega de tareas y entregue la tarea
   antes de la fecha límite.
