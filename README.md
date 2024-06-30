# Repositorio-IISSI2

# Examen Simulacro

Ex-Promoted: https://github.com/marrivbec/Ex-Promoted

# Examenes Parciales
Ex-AperturaRestaurantes: https://github.com/marrivbec/Ex-Apertura-Restaurante

Ex-NuevasCategorias: https://github.com/marrivbec/Ex-Nuevas-Categorias
- Creamos una nueva screen desde 0, además de controller y validation especificos de categorías.

Ex-Descuento: https://github.com/marrivbec/Ex-Descuento

Ex-Pinned: https://github.com/marrivbec/Ex-Pinned

Ex-Visibilidad: https://github.com/marrivbec/Ex-Visibilidad
- Lo principal es el trabajo con fechas.

# Examenes (con implementaciones útiles) 

Ex-MensajeParaFans: https://github.com/marrivbec/Ex-MensajeParaFans
- Destacamos la opción de poner un texto de varios colores que cambien cada cierto tiempo.

Ex-SortByPrice: https://github.com/marrivbec/Ex-SortByPrice
- Para ordenar mediante alguna propiedad del restaurante, tendremos que crear una función para el order del metodo que necesitemos del RestaurantController. En este caso : const chooseOrder = restaurant.sortByPrice ? [{ model: Product, as: 'products' }, 'price', 'ASC'] : [{ model: Product, as: 'products' }, 'order', 'ASC'], tenemos un operador ternario donde establecemos la condición que se tiene que cumplir (si es verdadero, la primera, en caso contrario la segunda).
  
Ex-RestauranteEconomico: https://github.com/marrivbec/Ex-RestauranteEconomico 
- Podemos comparar propiedades de un restaurante con otros: const averagePriceOfRestaurants = await Product.findOne({where: { restaurantId: { [Sequelize.Op.ne]: restaurantId } },attributes: [[Sequelize.fn('AVG', Sequelize.col('price')), 'avgPrice']]})

Ex-PromocionDescuento: https://github.com/marrivbec/Ex-PromocionDescuento
- Cuando nos piden aplicar descuentos o modificaciones al precio de los productos, debemos de crear una nueva propiedad a parte que guarde el contenido del precio base. Posteriormente modificaremos el precio aplicándole sus respectivos cambios, pero el precio base seguirá siendo el mismo. Para poder hacer esto tenemos que cambiar las funciones create (newProduct.basePrice = newProduct.price) y update (req.body.basePrice = req.body.price) de ProductController, en el update se pone con req.body ya que esto nos permite ver la petición del usuario cuando actualiza el restaurante.

Ex-MejorasEcosistema: https://github.com/marrivbec/Ex-MejorasEcosistema
- En este examen podremos:
    - Mostrar un mensaje que aparezca aleatoriamente.
    - Establecer un color pulsando un boton.
    - Establecer tamaño de texto pulsando un boton.

Ex-ProductoDestacado: https://github.com/marrivbec/Ex-ProductosDestacados
- Lo mas importante de este examen es una funcioón del controller que nos hace que solamente podamos marcar como destacado 5 productos, al marcar el 5 el primero que se destacó se quita y se pone el último destacado.



