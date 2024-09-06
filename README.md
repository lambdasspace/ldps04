## Lenguajes de Programación
### Evaluación Semanal 4

#### 📝 Instrucciones

- El semanal podrá resolverse **en equipos de 3**.
- Se deberá entregar por medio de GitHub Classroom a más tardar a las **23:59:59 del martes 10 de septiembre de 2024**. **No habrán prórrogas**. En caso de requerir más tiempo, se descontará un punto por cada día de entrega tardío.
- Cualquier duda podrá extenarse en la clase, por correo o por medio de Telegram en un horario de 9:00 a 18:00.
- Deberá entregarse en formato LaTeX (pueden consultar el siguiente paquete para generar reglas de inferencia: [`bussproofs.sty`](https://ctan.math.illinois.edu/macros/latex/contrib/bussproofs/BussGuide2.pdf)).
- No es necesario que vuelvan a escribir los ejercicios completos, basta con que los numeren y entreguen **en orden**.

#### 🚀 Ejercicios

1. Dadas las siguientes expresiones en sintaxis concreta de nuestro lenguaje **MiniLisp** (a) obtener su sintaxis abstracta y (b) evaluarlas usando las reglas de semántica natural. Todas las reglas podrán consultar en [Nota de Clase 9](https://lambdasspace.github.io/LDP/notas/ldpn09.pdf). Señalen en cada caso las variables libres y ligadas.

   *Nota:* Pueden hacerlo a mano y colocar una foto en su PDF final.

   - Expresión 1:

      ```lisp
      (let (a 5)
        (let (b (+ a 2))
          (let (c (- b 1))
            (let (foo (+ c 3))
              (let (goo (- foo a))
                (+ goo b))))))
      ```

   - Expresión 2:

      ```lisp
      (let (y (+ x (not 1))) 
         (let (x 5)
            (+ y x)))
      ```

   - Expresión 3:

      ```lisp
      (let (x 1)
        (let (y 2)
          (let (z (+ x y))
            (let (a (not #f))
              (let (b (+ a z))
                (+ b z))))))
      ```


2. Dados los siguientes términos λ, da una expresión equivalente por medio de currificación.

   - `λxy.xy`
   - `λxy.λzw.xyzw`
   - `λab.(λcd.ac)(λef.bf(λxyz.e))`

3. Dadas las siguientes expresiones, da una α-equivalencia para cada una de forma tal que todas las variables de ligado sean distintas. Indica en cada caso las variables libres y ligadas.

   - `λx.λy.λx.xy`
   - `(λx.λy.xy)(λy.λx.yx)`
   - `λa.λb.(λx.λy.ay)(λy.λx.by)`