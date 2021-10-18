# Cours HTML et CSS

```html
<!DOCTYPE html><!--norme html 5-->
<html lang="fr" dir="ltr">
    <head>
        <meta charset="UTF-8">
        <meta name="description" content="cours html et css...">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Cours html</title>
        <link rel="icon" type="image/png" href="./asset/file_type_html_icon_130541.png">
        <link rel="stylesheet" type="text/css" href="./css/style.css">
    </head>

    <body>
        <header>
            <h1>&lt;/&gt;Cours html<sup>5</sup> &amp; Css<sub>3</sub></h1>
        </header>
        <main>
            <section>
                <h2>Présentation: lire l'article &#187;</h2>
                <p><strong>Lorem ipsum dolor sit amet</strong> <b>la première section</b>.</p>
                <abbr title="HyperTextMarkupLanguage">HTML</abbr>
                le <time datetime="2021-09-27">27/09/2021</time>
            </section>

            <section>
                <h2>Liste des langages</h2>
                <p>Lorem ipsum dolor sit amet.
                    <del>XHTML</del> HTML<sup>5</sup>
                </p>
            </section>

            <section>
                <h2>Liste des tâches</h2>
                <!--liste ordonnées display block-->
                <ul>
                    <li>javascript</li><!--display-list-item-->
                    <li>Css</li>
                    <li>Html</li>
                </ul>
                <ol type="A"> 
                    <li>javascript</li><!--display-number-or-letter-list-item-->
                    <li>Css</li>
                    <li>Html</li>
                </ol>
            </section>

            <section>
                <h2>Liste des commentaires</h2>
                <!--liste déf-->
                <dl>
                    <dt>Bonjour</dt>
                    <dd>Coucou</dd>
                </dl>
                <p>Lorem ipsum dolor sit amet.</p>
            </section>

            <section>
                <h2>Le terminal</h2>
                <p>Lorem ipsum dolor sit amet.</p>
            </section>

            <section>
                <figure>
                    <img src="./asset/15621593492703_Colossus.jpg" alt="computer">
                <figcaption>
                    <h3>Notes historiques</h3>
                    <p>Il faut attendre 1946 et l’ENIAC (Electronic Numerical Integrator and Computer) conçu par Presper Eckert et John William Mauchly pour voir apparaître le premier ordinateur entièrement électronique construit pour être Turing-complet.
                        Si on recherche plus loin le tout premier Ordinateur appelé machine à calculer a été inventé par le Britannique Charle Babbage et perfectionné ensuite par Alain Turing que pendant la second guerre mondiale fût le seul a pouvoir déchiffrer la fameuse machine allemande Enigma.
                        Alain Turing ouvre la voie au premier ordinateur programmable dans les années qui suivent.
                        IBM se lance dans la course et en 1952 invente sa première machine à calculer programmable: le 701.
                        Entre les années 1960 et '70 ce fût la course au perfectionnements de ces machines doté également d’un microprocesseur et surtout à la miniaturisation car les ordinateurs de l’époque occupaient une pièce entière. Le seul point d’acces pour communiquer et programmer un ordinateur était le terminal: pas d’interface graphique comme aujourd’hui.</p>
                </figcaption>
                </figure>
            </section>
        </main>

        <footer>
            <p>&copy; - ITIC - WebPage - 2021</p>
        </footer>
    </body>
</html>
```

```css
/*
-reset css
-tailles
-marges
-padding
-link
1px=0.06rem
*/

html{ /*sélecteur(élément) propriété valeur*/
    font-size: 62.5%;/*10.000rem root em 10px*/
}
body{
    font: 1.6rem sans-serif; /* 16px */
    margin: 0;
}

h1,h2,h3,p,ol,ul,figure,dl{
    margin: 0;
    padding: 0;
    list-style-type: none;
}

h1,h2,h3{
    font-weight: normal;
}
/* thème*/
/*palette graphique*/
:root{
    --color-default: rgb(0, 0, 0);
    --color-header-text: #fff ;
    --color-primary:#5298c6;
    --color-alert:#c0392b;
    --color-sucess:#068a22;
    --color-warning:rgba(253,203,110,1.0);
}
/* variable appelée*/
header{
    background-color: var(--color-default);
    line-height: 6.0rem;
}
header > h1{
    color: var(--color-header-text);
    text-align: center;
}
main{
    max-width: 80.0rem;
    border: solid .1rem transparent;
    padding: 1.0rem;
    margin: 5.0rem auto 1.0rem;
    box-shadow: 0 0 1.0rem rgb(161,159,159);
}
figure > img{
    display: block;
    width: 100%;
    margin: .1rem;
}
section h2, section figure figcaption h3{
    background-color: var(--color-primary);
    color: var(--color-header-text);
    line-height: 4.5rem;
    padding: .5rem;
    font-size: x-large;
}
section p{
    line-height: 2.6rem;
}
/* placer les icones*/
section h2::before{
    content: '\2714';
    margin-right: .3rem;
}
main section + section h2{
    background-color: var(--color-alert);
}
main section:last-child h2{
    background-color: #ccc;
    color: #222;
}
main section:nth-child(2) h2{
    background-color: var(--color-sucess);
}
main section:nth-of-type(3) h2{
    background-color: var(--color-warning);
    color: #222;
}
main section:nth-child(5) h2{
    background-color: #ccc;
    color: #222;
}
section figure figcaption h3{
    background-color: rgb(245,135,9);
    color: #222;
}
footer *{
    text-align: center;
    color: #999;
}
/* responsive*/
@media screen and (max-width:70.0rem){
    main,footer{
        margin: .1rem;
    }
    header h1{
        background-color: rgb(189, 40, 40);
        font-size: x-large;
    }
    section h2, section figure figcaption h3{
        font-size: large;
    }
    section figure figcaption p, section p {
        text-align: justify;
    }
    footer{
        min-height: 20vh; /* hauteur 1/20 d'écran */
        display: grid;
        align-items: center;
    }
}
@media screen and(orientation:landscape) {
    header h1{
        background-color: #222;
        font-size: xx-large;
    }
}
```