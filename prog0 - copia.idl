pro prog0 ;Inicio del programa

;Tipo de datos: byte, integer, Longword integers, Floating point, Double-precision floating, Complex floating,
; r1=Intarr(5,5)      ; Integer array
; r2=Fltarr(5,5)      ; Floating point array
; r3=Bytarr(5,5)      ; Byte array
; r4=Complexarr(5,5)  ; Complex floating array,
;
;print, r1, 'r1'
;;print, r2, 'r2'
;;print, r3, 'r3'
;;print, r4, 'r4'
;
;r5=Indgen(5,5)
;r6=Findgen(5,5)
;;print,r5,'r5'
;
;    ;Lectura de la imagen
;    ans4a ='C:\Users\1046986683\Documents\Ciencia de Imagenes\Imagenes\Clase1\Fig1.07(b).jpg'
;    READ_JPEG,ans4a,image
;    tamanio=Size(image)
;    ;Dimension (2), pixeles en x(360), pixeles en y(414), tipo de numero (1), numero total de pixles (149040)
;    print,tamanio,'dimensiones de la imagen'
;    nx=tamanio(1) & ny=tamanio(2); nx=Numero de pixeles en x, ny=Numero de pixeles en y
;    Window,0,Xpos=0,Ypos=0,Xsize=nx,Ysize=ny,Title=ans4a ;Despliega una imagen;
;    Tvscl,image

;--------------------------------------------------------------------------------------------------------------------------------------------------
;  ;Visualizacion en 3D
;   xsurface,image
;  ;Cortar una imagen
;------------------------------------------------------------------------------------------------------------------------------------------------------
; Ciclos For
;
; imag2=bytarr(nx,ny)
;
; For j = 0,nx-1 Do Begin
;  For k = 0,ny-1 Do Begin
;   If(k lt ny/2) Then Begin
;     imag2(j,k)=255-image(j,k)
;   EndIf
;   If(k ge ny/2) Then Begin
;      imag2(j,k)=image(j,k)
;   EndIf
;  EndFor
; EndFor
;;
;;
;  Window,3,Xsize=nx,Ysize=ny,Title='Negativo'
;  Tvscl,imag2
;;;;;
;For j = 0,nx-1 Do Begin
; For k = 0,ny-1 Do Begin
;      If (j eq k) and (j gt 1) and (k gt 10) Then Begin
;;;Relational operadores: Equal to(EQ), Greater than or equal to (GE), Greter than(GT), Less than or equal to(LE)
;;                       ;Less than(LT),Not equal to(NE)
;        image(j,k)=0
;      EndIf
; EndFor
;EndFor
;;
;Window,4,Xpos=400,Ypos=0,Xsize=nx,Ysize=ny,Title='Imagen modificada'
;Tvscl,image


;-----------------------------------------------------------------------------------------------------------------------------------------------
;Ciclo While

;counter = 0
;
;Repeat Begin
;
;    counter = counter + 1
;
;print,counter,'contador'
;
;w =where(image eq 255,nmax) ;contraste de la imagen
;
;image(w)=0
;
;image=Bytscl(image)
;
;Window,4,Xpos=400,Ypos=0,Xsize=nx,Ysize=ny,Title=counter
;Tvscl,image
;;wait,0.1
;Endrep Until (counter Eq 30) or (nmax=0)

;---------------------------------------------------------------------------------------------------------------------------------------------------
;Para cortar una imagen

;nmar=3 & marcasx=fltarr(nmar) & marcasy=fltarr(nmar)
;
;print,marcasx,'x'
;print,marcasy,'y'
;
; For i=0,nmar-1 Do Begin
;   cursor,a,b,/device
;   wait,1
;   marcasx(i)=a & marcasy(i)=b
;   print,'marca', i, a,b
; EndFor
;
;xmax=max(marcasx) & xmin=min(marcasx) & ymax=max(marcasy) & ymin=min(marcasy)
;;
;lx2=xmax-xmin+1 & ly2=ymax-ymin+1
;
;imag1=bytarr(lx2,ly2)
;
;imag1(0:lx2-1,0:ly2-1)=image(xmin:xmax,ymin:ymax)
;
;imag2=image
;
;imag2(xmin:xmax,ymin:ymin+1)=255
;imag2(xmin:xmax,ymax:ymax+1)=255
;imag2(xmin:xmin+1,ymin:ymax)=255
;imag2(xmax:xmax+1,ymin:ymax)=255
;
;
;Window,1,Xpos=0,Ypos=0,Xsize=nx,Ysize=ny,Title='Imagen con contraste'
;Tvscl,imag2
;
;Window,12,Xpos=400,Ypos=0,Xsize=nx,Ysize=ny,Title='Imagen sin contraste'
;Tv,imag2
;
;Window,3,Xpos=800,Ypos=0,XSIZE=lx2, YSIZE=ly2, TITLE='Imagen cortada'
;Tv,imag1
;
;nombre2='C:\Users\1046986683\Documents\Ciencia de Imagenes\Imagenes\Clase1\modificada.jpg'
;WRITE_JPEG, nombre2,imag2,QUALITY=100

;-----------------------------------------------------------------------------------------------------------------------------------------------------------
;Obtencion de coordenadas bidimensionales de los pixeles
;  pix100=Where(image eq 100,nb)
;  x = pix100 mod nx & y = pix100/nx;Para encontrar los subindices bidimensionales
;  pos=fltarr(2,nb)
;  pos(0,0:nb-1)=x(0:nb-1)
;  pos(1,0:nb-1)=y(0:nb-1)
;
; image(pix100)=255
; print,pos,'coordenadas'
; Window,10,XSIZE=lx2, YSIZE=ly2, TITLE='Pixeles con un nivel de gris de 100'
; Tv,image
; print,pix100,'pixeles que tienen un nivel de gris de 100'
;--------------------------------------------------------------------------------------------------------------------------------------------------------
;Subroutinas
;lx=250 & ly=250 & sigma=100
;mask=mascara(lx,ly,sigma);Se crea una mascara gaussiana
;
;Window,5,Xsize=lx,Ysize=ly,Title='mascara'
;Tvscl,mask
;-----------------------------------------------------------------------------------------------------------------------------------------------------------
;Graficas
;w=100
;
;y1 =findgen(w)
;
;print,y1,'y1'
;y2 =findgen(w)
;y1=Sin(y1)
;y2=Cos(y2)
;Window,6,Xpos=800,Ypos=0,Xsize=500,Ysize=500,Title='mascara'
;Plot,y1,PSYM=5
;Oplot,y2
;--------------------------------------------------------------------------------------------------------------------------------------------------------
;Abrir una imagen a color
nombreI='C:\Users\1046986683\Documents\Ciencia de Imagenes\Imagenes\Clase1\bld228a1.jpg'
READ_JPEG, nombreI,a,True=1   ;Read and display a JPEG true-color image on a true-color display.
tamano=size(a)
print,tamano,'tamano'
;print,tamano,'tamano'
nx=tamano(2) & ny=tamano(3)
print,nx,ny,'----------'

Window,8,Xsize=nx,Ysize=ny,Title='Original a color en RGB'
Tv,a,True=1

r=bytarr(nx,ny) &  g=bytarr(nx,ny) &  b=bytarr(nx,ny)
r(*,*)=a(0,*,*) & g(*,*)=a(1,*,*) & b(*,*)=a(2,*,*)

Window,10,Xsize=nx,Ysize=ny,Title='Red'
tvscl,r
;
Window,11,Xsize=nx,Ysize=ny,Title='Green'
tvscl,g
;
Window,12,Xsize=nx,Ysize=ny,Title='Blue'
tvscl,b
;

print,a(0,0:3,0:3),'matriz'

a(0,*,*)=0
a(2,*,*)=0
;;Window,15,Xsize=nx,Ysize=ny,Title='A color en RGB'
;;Tv,a,True=1
;
;;Guardar una imagen procesada
;nombre2='C:\Users\samsung\Desktop\Clase1\green1.jpg'
;WRITE_JPEG, nombre2,r,QUALITY=100
;
;print,nombre2,'nombre2'

print,'Ya termine'

END
;===========================================================================================================================================================
function mascara,nx,ny,sigma
mf=Fltarr(nx,ny)

  For j=0,nx-1 Do Begin
            For k=0,ny-1 Do Begin
      mf(j,k)=1.0*exp(-(SQRT((j-nx/2)^2+(k-ny/2)^2))^2/(2*(sigma)^2))
            EndFor
  EndFor

xsurface,mf
Return,mf
End
;===========================================================================================================================================================











