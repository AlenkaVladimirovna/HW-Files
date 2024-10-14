# Домашнее задание к лекции «Потоки ввода-вывода. Работа с файлами. Сериализация»
## Задание 1. Установка


```
import java.io.File;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        File dirl = new File("C://Games");

        File src = new File(dirl, "src");
        if (src.mkdir())
            System.out.println("Каталог src создан");

        File res = new File(dirl, "res");
        if (res.mkdir())
            System.out.println("Каталог res создан");

        File savegames = new File(dirl, "savegames");
        if (savegames.mkdir())
            System.out.println("Каталог savegames создан");

        File temp = new File(dirl, "temp");
        if (temp.mkdir())
            System.out.println("Каталог temp создан");

        File main = new File(src, "main");
        if (main.mkdir())
            System.out.println("Каталог main создан");

        File test = new File(src, "test");
        if (test.mkdir())
            System.out.println("Каталог test создан");

        File drawables = new File(res, "drawables");
        if (drawables.mkdir())
            System.out.println("Каталог drawables создан");

        File vectors = new File(res, "vectors");
        if (vectors.mkdir())
            System.out.println("Каталог vectors создан");

        File icons = new File(res, "icons");
        if (icons.mkdir())
            System.out.println("Каталог icons создан");

        File myFileMain = new File("main//Main.java");
        try {
            if (myFileMain.createNewFile())
                System.out.println("Файл Main.java создан");
        } catch (IOException ex) {
            System.out.println(ex.getMessage());
        }

        File myFileUtils = new File("main//Utils.java");
        try {
            if (myFileUtils.createNewFile())
                System.out.println("Файл Utils.java создан");
        } catch (IOException ex) {
            System.out.println(ex.getMessage());
        }

        File myFileTemp = new File("temp//temp.txt");
        try {
            if (myFileTemp.createNewFile())
                System.out.println("Файл tmp.txt создан");

        } catch (IOException ex) {
            System.out.println(ex.getMessage());
        }
    }


}

```

у меня вопрос: почему не создается файл?

программа выдает:

```
Системе не удается найти указанный путь

```