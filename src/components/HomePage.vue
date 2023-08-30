<template>
    <div class="pic-and-bio">
        <div class="left-side">
            <p class="bio">Hello and welcome! My name is Lucas Carter, and I’m a recent graduate from Duke University, where I earned my Bachelor of Science degree in computer science, with minors in French and linguistics. I’m currently on the search for a software engineering job in The Triangle area, and would love to hear about any and all opportunities!<br><br>Contact me:<br><a href="mailto: lucascarter1234@gmail.com">lucascarter1234@gmail.com</a></p>
        </div>
        <div class="right-side">
            <img src="../assets/LucasHeadshotCircle.png" id="my-photo" class="pic"/>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>

#my-photo {
    height: 25em;
    width: 25em;
}
.pic-and-bio {
    padding: 3em;
    margin: 3em;
    padding-top: 1.5em;
    margin-top: 1.5em;
    text-align: center;
    display: flex;
    /*font-weight: 200;*/
}
.left-side {
    width: 75%;
    padding: 1em;
}
.right-side {
    flex-grow: 1;
}
.bio {
    font-size: 2em;
    float: right;
    text-align: left;

}
.pic {
    border-radius: 50%;
    text-align: center;
    shape-outside: circle(25%);
    float: left;
    padding-top: 0.5em;
}
p {
    margin: 0%;
}
/* Media query for mobile devices */
@media (max-width: 768px) {
    .pic-and-bio {
        flex-direction: column;
        align-items: center;
        padding: 1em;
        margin: 1em;
    }
    .left-side, .right-side {
        width: 100%;
    }
    .bio {
        font-size: 1.5em; /* Adjust font size */
        text-align: center;
        float: none;
    }
    #my-photo {
        height: 15em;
        width: 15em;
    }
}


</style>