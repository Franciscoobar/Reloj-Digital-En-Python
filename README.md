# Reloj-Digital-En-Python
Reloj digital en python utilizando libreria  tkinter
import tkinter as tk
import time

ventana = tk.Tk()
ventana.title("Reloj Digital")

def actualizar_reloj():
    hora_actual = time.strftime("%H:%M:%S")
    etiqueta.config(text=hora_actual)
    etiqueta.after(1000, actualizar_reloj)

etiqueta = tk.Label(ventana, font=("Arial", 50), bg="black", fg= "white")
 
etiqueta.pack(anchor="center")

actualizar_reloj()

ventana.mainloop()
