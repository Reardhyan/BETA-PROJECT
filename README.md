# BETA-PROJECT

#include <iostream>
using namespace std;

int main() {
    int Array[] = {1, 2, 3, 4, 5};
    int n = sizeof(Array) / sizeof(Array[0]);
    int menu;
    do {
        cout << "Menu Utama:\n";
        cout << "1. Input Data\n";
        cout << "2. Tampilkan Data\n";
        cout << "3. Distribusi Frekuensi\n";
        cout << "4. Statistik\n";
        cout << "5. Keluar\n";
        cout << "Masukkan pilihan Anda: ";
        cin >> menu;
        switch (menu) {
            case 1:
                cout << "Masukkan banyak data: ";
                cin >> n;
                for (int i = 0; i < n; i++) {
                    cout << "Data ke-" << i + 1 << ": ";
                    cin >> Array[i];
                }
                break;
            case 2:
                cout << "Data yang telah dimasukkan:\n";
                for (int i = 0; i < n; i++) {
                    cout << Array[i] << " ";
                }
                cout << endl;
                break;
            case 3:
                int range_1 = 0, range_2 = 0, range_3 = 0, range_4 = 0, range_5 = 0;
                for (int i = 0; i < n; i++) {
                    if (Array[i] >= 0 && Array[i] <= 20) {
                        range_1++;
                    } else if (Array[i] > 20 && Array[i] <= 40) {
                        range_2++;
                    } else if (Array[i] > 40 && Array[i] <= 60) {
                        range_3++;
                    } else if (Array[i] > 60 && Array[i] <= 80) {
                        range_4++;
                    } else if (Array[i] > 80 && Array[i] <= 100) {
                        range_5++;
                    }
                }
                cout << "Range 1: " << range_1 << endl;
                cout << "Range 2: " << range_2 << endl;
                cout << "Range 3: " << range_3 << endl;
                cout << "Range 4: " << range_4 << endl;
                cout << "Range 5: " << range_5 << endl;
                break;
            case 4:
                double total = 0;
                for (int i = 0; i < n; i++) {
                    total += Array[i];
                }
                double mean = total / n;
                cout << "Mean: " << mean << endl;
                int min = Array[0], max = Array[0];
                for (int i = 0; i < n; i++) {
                    if (Array[i] < min) {
                        min = Array[i];
                    }
                    if (Array[i] > max) {
                        max = Array[i];
                    }
                }
                cout << "Minimum: " << min << endl;
                cout << "Maximum: " << max << endl;
                break;
            case 5:
                cout << "Terima kasih telah menggunakan program ini.\n";
                break;
            default:
                cout << "Pilihan tidak valid. Silakan coba lagi.\n";
        }
    } while (menu != 5);
    return 0;
}
