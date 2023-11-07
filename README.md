# Tugas_OOP4

Nama : Riska Hidayah Putri

NIM : 312210102

Kelas : TI.22.B1

Mata Kuliah : Pemrograman Orientasi Objek

Tugas Inheritance : latihan class Mahasiswa dengan setter dan getter.

Codingannya :

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace TugasPert7
{
    public class Pegawai
    {


        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {

        private double tunjangan;

        public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
        public double getTunjangan() { return this.tunjangan; }

        public new void cetakinfo()
        {

            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);

        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);


        }

    }
    class program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("==== PEGAWAI ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Riska Hidayah Putri");
            pegawai.setGajiPokok(5000000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER ====");
            manager Manager = new manager();
            Manager.setNama("Riska Hidayah Putri");
            Manager.setGajiPokok(30000000);
            Manager.setTunjangan(10000000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER ====");
            Programmer programer = new Programmer();
            programer.setNama("Riska Hidayah Putri");
            programer.setGajiPokok(50000000);
            programer.setBonus(10000000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}
```

Hasilnya :

<img width="867" alt="oop4" src="https://github.com/riskahidayahputri/Tugas_OOP4/assets/115815582/efba40d4-74b9-43e9-8dc8-3890fb8d432d">
