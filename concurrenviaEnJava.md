Introducción: Semáforos Binarios para Exclusión Mutua

Los semáforos son construcciones de control de concurrencia. Son usados para controlar el acceso a un recurso compartido o llevar a cabo una cierta acción al mismo tiempo. Un semáforo gestiona un conjunto de permisos virtuales, cuyo número inicial es dado al crear el semáforo. Un semáforo BINARIO es un
semáforo que gestiona solo 1 permiso, con el cual dará acceso a la sección crítica a un hilo. Como
sólo gestiona un permiso, asegura la exclusión mutua, ya que mientras un hilo tenga ese permiso,
ningún otro hilo podrá adquirirlo.


Guía de uso
Para usar semáforos en Java se debe importar la clase 'java.util.concurrent.Semaphore'.
Las operaciones básicas para trabajar con semáforos son: – adquirir / acquire (Java) – liberar /
release (Java). Las actividades pueden adquirir un permiso (siempre que haya disponible) para
trabajar sobre una sección crítica y liberarlo cuando terminan. Si ningun permiso esta libre
entonces la operacion de adquirir (adquire) se bloquea hasta que un permiso este libre, sea
interrumpida o expire su tiempo. La operación de liberar un permiso (release) lo retorna al
semáforo. Un semáforo binario, se utiliza como un mutex (exclusión mutua).