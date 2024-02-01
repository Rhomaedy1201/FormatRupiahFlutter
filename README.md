Cara Membuat Format Rupiah menggunakan Flutter
#Contoh
<pre>
import 'package:intl/intl.dart';

class FormatCurrency {
  static String formatRp(dynamic number, int decimalDigit) {
    NumberFormat currencyFormatter = NumberFormat.currency(
      locale: 'id',
      symbol: 'Rp ',
      decimalDigits: decimalDigit,
    );
    return currencyFormatter.format(number);
  }

  static String formatNotRp(dynamic number, int decimalDigit) {
    NumberFormat currencyFormatter = NumberFormat.currency(
      locale: 'id',
      symbol: '',
      decimalDigits: decimalDigit,
    );
    return currencyFormatter.format(number);
  }
}

// cara menggunakan 
// FormatRupiah.formatRp(1000000, 2)
// FormatRupiah.formatNotRp(1000000, 2)
// FormatRupiah.formatNotRp(1000000, 0)

// hasil formatRp : Rp 1.000.000,00
// hasil formatNotRp : 1.000.000,00
// hasil jika menggunakan 0 : 1.000.000

</pre>
