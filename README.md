import tkinter as tk
from tkinter import messagebox

def simpan_data():
    nim = entry_nim.get()
    nama = entry_nama.get()
    alamat = entry_alamat.get()
    prodi = entry_prodi.get()
    jenis_kelamin = entry_jenis_kelamin.get()
    agama = entry_agama.get()

    detail_data = f"NIM: {nim}\nNama: {nama}\nAlamat: {alamat}\nProdi: {prodi}\nJenis Kelamin: {jenis_kelamin}\nAgama: {agama}"
    messagebox.showinfo("Detail Data", detail_data)

app = tk.Tk()
app.title("Aplikasi Data Mahasiswa")

# Label dan Entry untuk NIM
label_nim = tk.Label(app, text="NIM:")
entry_nim = tk.Entry(app)
label_nim.grid(row=0, column=0, padx=10, pady=5)
entry_nim.grid(row=0, column=1, padx=10, pady=5)

# Label dan Entry untuk Nama
label_nama = tk.Label(app, text="Nama:")
entry_nama = tk.Entry(app)
label_nama.grid(row=1, column=0, padx=10, pady=5)
entry_nama.grid(row=1, column=1, padx=10, pady=5)

# Label dan Entry untuk Alamat
label_alamat = tk.Label(app, text="Alamat:")
entry_alamat = tk.Entry(app)
label_alamat.grid(row=2, column=0, padx=10, pady=5)
entry_alamat.grid(row=2, column=1, padx=10, pady=5)

# Label dan Entry untuk Prodi
label_prodi = tk.Label(app, text="Prodi:")
entry_prodi = tk.Entry(app)
label_prodi.grid(row=3, column=0, padx=10, pady=5)
entry_prodi.grid(row=3, column=1, padx=10, pady=5)

# Label dan Entry untuk Jenis Kelamin
label_jenis_kelamin = tk.Label(app, text="Jenis Kelamin:")
entry_jenis_kelamin = tk.Entry(app)
label_jenis_kelamin.grid(row=4, column=0, padx=10, pady=5)
entry_jenis_kelamin.grid(row=4, column=1, padx=10, pady=5)

# Label dan Entry untuk Agama
label_agama = tk.Label(app, text="Agama:")
entry_agama = tk.Entry(app)
label_agama.grid(row=5, column=0, padx=10, pady=5)
entry_agama.grid(row=5, column=1, padx=10, pady=5)

# Tombol Simpan
tombol_simpan = tk.Button(app, text="Simpan", command=simpan_data)
tombol_simpan.grid(row=6, columnspan=2, padx=10, pady=10)

app.mainloop()
