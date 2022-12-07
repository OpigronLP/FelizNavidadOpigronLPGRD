<!DOCTYPEhtml >
< html  lang =" es " >
< cabeza >
    < juego de caracteres meta  =" UTF-8 " >
    < meta  http-equiv =" X-UA-Compatible " content =" IE=edge " >
    < meta  name =" viewport " content =" ancho=ancho-del-dispositivo, escala-inicial=1.0 " >
    < título > FELIZ NAVIDAD </ título >
    < estilo >
        cuerpo { fondo : negro; pantalla : cuadrícula; justificar-contenido : centro; alineación de texto : centro; }
        h1 { color : verdeamarillo;}
        p { color : verde azulado; }
        . estrella { tamaño de fuente :  100 px ; animación : colores 1 s infinito;}
        . rojo {
            color : rojo;
            transición : todo 1,5 s ;
            tamaño de fuente :  30 px ;
        }
        @keyframes colores {
            0 % { color : rojo;}
            33 % { color : verde;}
            66 % { color : rojo;}
            100 % { color : amarillo;}
        }
    </ estilo >
</ cabeza >
< cuerpo >
    < div  class =" estrella " > * </ div >
    < div  id =" árbol " > </ div >
    < h1 > ¡FELIZ NAVIDAD FERNANDA Y PRÓSPERO AÑO NUEVO 2023! </ h1 >
    < P > Te desea por Gerardo Ramonet Dorame, Felices Fiestas Fernanda, Que las luces de estas Fiestas Navideñas brillan con mucha esperanza en tu corazón. Tu siempre serás una reina para mí. </ P >
    < guión >
        var  hojas  =  "" ;
        [ 10 , 2 ] . paraCada ( fila  =>  {
            nueva  matriz ( fila ) . llenar ( '' ) . paraCada ( ( v , i )  =>  {
                hojas  +=  ( [
                    ... Matriz ( 9 - i ) . llenar ( "<span> </span>" ) ,
                    ... Matriz ( 1 + i * 2 ) . llenar ( "<span class='rojo'>*</span>" ) ,
                    ... Matriz ( 9 - i ) . llenar ( "<span> </span>" ) ,

                ] . unirse ( '' ) )
                hojas  +=  "<br>"
            } )
        } ) 
        documento _ getElementById ( "árbol" ) . HTML interno  =  hojas ;

        let  animacion  =  documento . querySelectorAll ( ".rojo" ) ;
        animacion _ HTML interno  =  hojas ;
        función  animar ( ) {
            for (  var  i  = 0  ;  i < animacion . length ;  i ++ ) {
                sea  ​​tiempo  =  i / 20  + 1 ;
                animación [ yo ] . estilo _ animacion  =  "colores" + tiempo + "s infinito"
            }
        }
        ventana _ addEventListener ( 'cargar' , animar )
        
    </ guión >
</ cuerpo >
</ html >
