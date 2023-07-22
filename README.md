# Ubuntu-Bildirim
basit bir ubuntu bildirim yollama kodu

## Method:

    public static void showNotification(String title, String message) {
        try {
            // Linux için bildirim oluşturmak için notify-send komutunu kullanıyoruz.
            String[] cmd = {"notify-send", title, message};
            ProcessBuilder processBuilder = new ProcessBuilder(cmd);
            processBuilder.start();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

# Kullanım:

        showNotification("Linux Bildirimi", "Merhaba! Bu bir modern Linux bildirimidir.");
