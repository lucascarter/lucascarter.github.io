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
    padding-top: 0;
}
.right-side {
    flex-grow: 1;
}
.bio {
    font-size: 2em;
    float: right;
    text-align: left;
    font-weight: 300;
    text-shadow: 2px 4px 7px rgba(115, 118, 124, 0.6);
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



</style>