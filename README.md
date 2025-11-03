# tugas-1
import java.util.Scanner;

public class tugasku {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // ==============================
        // Bagian 1: Perhitungan Biaya Ekspedisi
        // ==============================
        System.out.println("=== PROGRAM PERHITUNGAN BIAYA EKSPEDISI ===");

        System.out.print("Masukkan berat paket (kg): ");
        double berat = input.nextDouble();

        System.out.print("Masukkan jarak tempuh (km): ");
        double jarak = input.nextDouble();

        System.out.print("Masukkan panjang paket (cm): ");
        double panjang = input.nextDouble();

        System.out.print("Masukkan lebar paket (cm): ");
        double lebar = input.nextDouble();

        System.out.print("Masukkan tinggi paket (cm): ");
        double tinggi = input.nextDouble();

        double volume = panjang * lebar * tinggi;
        double biayaPerKg;

        // Menentukan biaya per kg berdasarkan jarak
        if (jarak <= 10) {
            biayaPerKg = 4250;
        } else {
            biayaPerKg = 6000;
        }

        double biaya = berat * biayaPerKg;

        // Tambahan biaya volume
        if (volume > 100) {
            biaya += 50000;
        }

        System.out.println("\n=== HASIL PERHITUNGAN ===");
        System.out.println("Volume paket : " + volume + " cm^3");
        System.out.println("Biaya kirim  : Rp " + biaya);

        // ==============================
        // Bagian 2: Menentukan Ganjil atau Genap
        // ==============================
        System.out.println("\n=== CEK BILANGAN GANJIL / GENAP ===");
        System.out.print("Masukkan sebuah bilangan: ");
        int bilangan = input.nextInt();

        if (bilangan % 2 == 0) {
            System.out.println(bilangan + " adalah bilangan GENAP.");
        } else {
            System.out.println(bilangan + " adalah bilangan GANJIL.");
        }

        input.close();
    }
}
Program di atas memiliki **dua fungsi utama**:

1. **Menghitung biaya ekspedisi**

   * Input: berat, jarak, panjang, lebar, dan tinggi paket.
   * Jika jarak ≤ 10 km → biaya/kg = Rp 4.250
     Jika jarak > 10 km → biaya/kg = Rp 6.000
   * Jika volume paket > 100 cm³ → tambah biaya Rp 50.000
   * Hasil akhir: menampilkan volume dan total biaya kirim.

2. **Menentukan bilangan ganjil atau genap**

   * Input: satu bilangan bulat.
   * Jika `bilangan % 2 == 0` → genap, selain itu → ganjil.

