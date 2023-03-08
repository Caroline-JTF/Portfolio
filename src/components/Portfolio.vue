<template>
    <section class="grid">
        <a 
            href="https://github.com/Caroline-JTF/CoffeeAndBookShop" 
            target="_blank" 
            class="photo-1">
            <figcaption>
                <span>Coffee And Book </span>
                <span>Projet de formation</span>
                <span>Non mis en ligne</span>
            </figcaption>
        </a>
        <a 
            href="https://caroline-jtf.github.io/Convertisseur_Coordonnees_Minecraft/" 
            target="_blank" 
            class="photo-2">
            <figcaption>
                <span>Convertisseur </span>
                <span>de Coordonnees</span>
                <span>Sur le jeu Minecraft</span>
            </figcaption>
        </a>
        <a 
            href="https://caroline-jtf.github.io/To_Do_List_DreamLight_Valley/" 
            target="_blank" 
            class="photo-3">
            <figcaption>
                <span>To Do List </span>
                <span>Conversations quotidiennes</span>
                <span>Sur le jeu DreamLight Valley</span>
            </figcaption>
        </a>
	</section>
</template>

<script>
    export default {
        name: "Portfolio",

        data() {
            return {
                scale: 1
            }
        },
        methods: {
            zoomIn() {
                this.scale += 0.1 
            },
            zoomOut() {
                if (this.scale > 1) {
                    this.scale -= 0.1
                }
            }
        }
    }
</script>

<style>
    a{
        position: relative;
    }

    figcaption {
	position: absolute;
	top:0;
	left: 0;
	right: 0;
	bottom: 0;
	opacity: 0;
	background-color: rgba(0, 0, 0, 0.5);
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	color: white;
	transition: 0.7s all;
    }

    figcaption span {
        font-size: 0.8em;
        margin: 0 5em;
    }

    figcaption::after{
        content:"";
        position: absolute;
        right: 1em;
        left: 1em;
        top: 1em;
        bottom: 1em;
        border: 1px solid white;
    }

    a:hover figcaption {
        opacity: 1;
    }

    .grid {
        display: grid;
        grid-template-rows: repeat(auto, 1fr);
        grid-template-columns: repeat(3, 1fr);
        gap: 1em;
        width: 90vw;
        margin: 1em auto;
    }

    .grid [class*="photo"] {
        grid-area: auto;
        height: 250px;
        background-size: cover;
        background-repeat: no-repeat;
        background-position-x: center;
        background-position-y: end;
        transition: transform .1s;
    }

    .grid .photo-1{
        background-image: url('../assets/images/coffeeAndBook.png');
    }

    .grid .photo-2{
        background-image: url('../assets/images/minecraft.png');
    }

    .grid .photo-3{
        background-image: url('../assets/images/dreamlightValley.png');
    }

    @media screen and (max-width:1024px) {
        .grid{
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media screen and (max-width:425px) {
        .grid{
            grid-template-columns: repeat(1, 1fr);
        }
    }

</style>