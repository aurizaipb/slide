---
title: Markdown
author: Auriza Akbar
institute: Ilmu Komputer IPB
date: 2017
theme: Dresden
header-includes:
    - \renewcommand{\figurename}{Gambar}
    - \renewcommand{\tablename}{Tabel}
---

# Motivasi

## Mengapa Markdown?

- mudah ditulis
- mudah dibaca
- tanpa *markup*
- teks biasa (.md)

## Populer

- GitHub
- StackOverflow
- WordPress
- Moodle (LMS)
- ...

# Sintaks

## Metadata[^yaml]

```yaml
---
title: Markdown
author: Auriza Akbar
institute: Ilmu Komputer IPB
date: 2017
theme: Dresden
header-includes:
    - \renewcommand{\tablename}{Tabel}
    - \renewcommand{\figurename}{Gambar}
---
```

[^yaml]: *lihat* <http://pandoc.org/MANUAL.html#variables-set-by-pandoc>

## Paragraf

```markdown
Sebuah paragraf.

Paragraf selanjutnya setelah satu baris kosong.
```


## Paragraf

`\[space]`
: *non-breaking space*

`\[newline]`
: *hard line-break*

`--`
: *en dash*

`---`
: *em dash*

`...`
: *ellipsis*

```markdown
Harga emas saat ini sekitar Rp\ 550\ 000 per gram,
wajib dikeluarkan zakatnya jika sudah mencapai
*nishab* 85 gram dan *haul* satu tahun ...
```

Harga emas saat ini sekitar Rp\ 550\ 000 per gram,
wajib dikeluarkan zakatnya jika sudah mencapai
*nishab* 85 gram dan *haul* satu tahun ...


## Format Inline

`*text*`
: *emphasis*

`**text**`
: **strong emphasis**

`~~text~~`
: ~~strike out~~

`H~2~O`
: H~2~O

`x^2^`
: x^2^

`` `code` ``
: `code`


## Header

~~~markdown
# Header 1

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6
~~~


## Kutipan

```markdown
> There are six levels of knowledge:
>
> 1. excellence in asking questions,
> 2. excellence in paying attention and listening,
> 3. excellence in understanding,
```

> There are six levels of knowledge:
>
> 1. excellence in asking questions,
> 2. excellence in paying attention and listening,
> 3. excellence in understanding,
> 4. memorizing,
> 5. teaching, and
> 6. implementing it and appreciating its boundaries.



## Kode

````
```c
int main() {
    printf("Hello world!\n");
    return 0;
}
```
````

```c
int main() {
    printf("Hello world!\n");
    return 0;
}
```

## List

```markdown
- one
- two
- three
```

- one
- two
- three


## List Bernomor

```markdown
1. one
2. two
3. three
```

1. one
2. two
3. three


## List Bersarang

```markdown
1. one
    - indent
    - four
    - spaces
2. two
3. three
```

1. one
    - indent
    - four
    - spaces
2. two
3. three


## List Definisi

```markdown
awkward
: causing difficulty; hard to do or deal with.

goggle
: look with wide open eyes.
```

awkward
: causing difficulty; hard to do or deal with.

goggle
: look with wide open eyes.


## Link

- Otomatis

    ```markdown
    Kunjungi <http://cs.ipb.ac.id> atau email ke
    <cs@ipb.ac.id>.
    ```

    Kunjungi <http://cs.ipb.ac.id> atau email ke <cs@ipb.ac.id>.

- *Inline*

    ```markdown
    Kunjungi [Ilkom IPB](http://cs.ipb.ac.id) atau
    kirim [email](mailto:cs@ipb.ac.id).
    ```

    Kunjungi [Ilkom IPB](http://cs.ipb.ac.id) atau kirim [email](mailto:cs@ipb.ac.id).

## Link

- *Reference*

    ```markdown
    Kunjungi [Ilkom IPB] atau kirim [email].

    [ilkom ipb]: http://ipb.ac.id
    [email]: mailto:cs@ipb.ac.id
    ```

    Kunjungi [Ilkom IPB] atau kirim [email].

    [ilkom ipb]: http://ipb.ac.id
    [email]: mailto:cs@ipb.ac.id


## Catatan Kaki

```markdown
Penulis yaitu Dr Heru Sukoco[^hrs] dan
Dr Sugi Guritman[^sgn].

[^hrs]: Departemen Ilmu Komputer IPB
[^sgn]: Departemen Matematika IPB
```

Penulis yaitu Dr Heru Sukoco[^hrs] dan
Dr Sugi Guritman[^sgn].

[^hrs]: Departemen Ilmu Komputer IPB
[^sgn]: Departemen Matematika IPB


## Gambar

~~~markdown
![*A square map projection*.](quincuncial.jpg){width=40%}
~~~

![*A square map projection*.](quincuncial.jpg){width=40%}



## Tabel

~~~markdown
: Nilai tugas Penkom.

 NIM  Nama       Nilai
----- --------- ------
 001  Hanif         70
 002  Sarah         80
 003  Ahmad        100
~~~

: Nilai tugas Penkom.

 NIM  Nama       Nilai
----- --------- ------
 001  Hanif         70
 002  Sarah         80
 003  Ahmad        100


## Persamaan Matematika

~~~markdown
Untuk menulis persamaan, sama dengan \LaTeX. Misal
persamaan *inline* $x^2 + y^2 = 0$, atau persamaan
*displayed*:

$$ \sum_{i=0}^n A_i $$
~~~

Untuk menulis persamaan, sama dengan \LaTeX. Misal
persamaan *inline* $x^2 + y^2 = 0$, atau persamaan
*displayed*:

$$\sum_{i=0}^n A_i$$


## Persamaan Matematika

~~~markdown
Untuk persamaan *numbered*, langsung dengan sintaks
\LaTeX:

\begin{equation}
    \sum_{i=0}^n A_i
\end{equation}
~~~

Untuk persamaan *numbered*, langsung dengan sintaks
\LaTeX:

\begin{equation}
    \sum_{i=0}^n A_i
\end{equation}


## Lain-lain

Untuk sintaks yang tidak disediakan Markdown, bisa langsung menggunakan
sintaks \LaTeX, maupun HTML.

~~~latex
\textsc{Auriza Akbar}
~~~

\textsc{Auriza Akbar}

~~~html
<span style="font-variant:small-caps">Auriza Akbar</span>
~~~

<span style="font-variant:small-caps">Auriza Akbar</span>


# Kompilasi

## Pandoc

- Pandoc mengkonversi dari satu format markup ke yang lain
    - HTML
    - LaTeX dan PDF
    - EPUB
    - ODT dan DOCX
- Menggunakan *command line*
    - *lihat* <http://pandoc.org/README.html> untuk opsi lengkapnya


## Opsi Penting

`-o`
: *output*

`-t`
: *to* (format tujuan)

`-s`
: *standalone* (satu dokumen utuh)

`--mathml`
: konversi persamaan \LaTeX ke MathML


## Markdown ke HTML

~~~bash
pandoc -s -o output.html text.md

pandoc -s --mathml -o output.html text.md
~~~


## Markdown ke PDF

~~~bash
pandoc -o output.pdf text.md
~~~

## Markdown ke Slide PDF

~~~
pandoc -t beamer -o output.pdf slide.md
~~~


## Markdown ke Slide HTML

~~~
pandoc -s -t revealjs -o output.html slide.md
~~~

- `-t`: `slidy, dzlides, revealjs, s5, slideous`

<!--

- Untuk revealjs, unduh dahulu library-nya di [GitHub](https://github.com/hakimel/reveal.js/archive/master.zip)
    dan ekstrak ke direktori yang sama dengan slide HTML.

## Konversi Online

- <http://pandoc.org/try/>

-->

# FIN
