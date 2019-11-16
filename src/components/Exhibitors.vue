<template>
    <div class="grid gap_s collapse-p">
        <div class="span-6">
            <figure class="media">
                <img src="//picsum.photos/800/450/?random" alt="Photo via picsum.photos">
                <div class="text-mono mini-info">Image</div>
            </figure>
        </div>
        <div class="span-6">
            <figure class="media">
                <blockquote class="text-serif text-italic pa_m">
                    <p class="text_xl">Organizations which design systems are constrained to produce designs which are copies of the communication structures of these organizations.</p>
                    <p class="text_s ma-t_s">—Melvin Conway</p>
                </blockquote>
                <div class="text-mono mini-info">Text</div>
            </figure>
        </div>
    </div>
<!--    <div class="columns gap-no cols-4 cols-2-t collapse-p">-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-a flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">C</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <a href="#cambridge" class="span-auto self-center">Cambridge University Press</a>-->
<!--            </div>-->
<!--        </div>-->
<!--            <div id="cambridge" class="modal-window">-->
<!--                <div>-->
<!--                    <a href="#" title="Close" class="modal-close">&#215;</a>-->
<!--                    <h1>Cambridge University Press</h1>-->
<!--                    <div class="ma-b_xs ma-t_s">-->
<!--                        Booth Number - -->
<!--                        <span style="text-decoration: underline">A12</span>-->
<!--                    </div>-->
<!--                    <div class="ma-b_xs ma-t_s">-->
<!--                        <a href="https://www.cambridge.org" style="text-decoration: underline">https://www.cambridge.org</a>-->
<!--                    </div>-->
<!--                    <div class="text_l read_l ma-t_m">-->
<!--                        <p>Cambridge University Press is a department of the University of Cambridge and is both an academic and educational publisher. With a global sales presence, publishing hubs, and offices in more than 40 countries, it publishes over 50,000 titles by authors from over 100 countries. Its publishing includes academic journals, monographs, reference works, textbooks, and English language teaching and learning publications. It also prints and sells Bibles. Cambridge University Press is a charitable enterprise that transfers part of its annual surplus back to the University of Cambridge.</p>-->
<!--                    </div>-->
<!--                    <div class="read_l  ma-t_l">-->
<!--                        <h3 id="">Recommended Books</h3>-->
<!--                        <ul class="gap_no ma-t_xs bo-t_xs">-->
<!--                            <li v-for="book in books" v-bind:key="book">-->
<!--                                <a href="#" class="block-link bo-t_px">{{ book.message }}</a>-->
<!--                            </li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                            <li><a href="#" class="block-link bo-t_px">Down the Rabbit-Hole</a></li>-->
<!--                        </ul>-->
<!--                    </div>-->

<!--                </div>-->
<!--            </div>-->

<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-t flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">A</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Association of Taipei Publishers</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-u flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">A</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Argentina Consulate General</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-v flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">H</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Hong Kong University Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-w flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">A</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Abilene Christian University Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-x flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">U</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">University of Adelaide Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-y flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">K</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Khazar University Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-z flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">P</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Pontifical Catholic University of Chile Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-0 flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">T</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Tsinghua University Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-1 flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">D</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Dalian University of Technology Press</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-2 flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">U</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">University of Valle Publishing Program</div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">-->
<!--            <div class="span-auto pa-l_xs">-->
<!--                <div class="bg-3 flex ra-circle bo_px width_l height_l">-->
<!--                    <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">P</div>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="ma-l_s text-clip flex">-->
<!--                <div class="span-auto self-center">Presses Universitaires de France</div>-->
<!--            </div>-->
<!--        </div>-->
<!--    </div>-->
</template>

<script>
    export default {
        name: "Exhibitors"
    }
    // var example1 = new Vue({
    //     el: '#example-1',
    //     data: {
    //         items: [
    //             { message: 'Foo' },
    //             { message: 'Bar' }
    //         ]
    //     }
    // })
</script>

<style scoped>
    .modal-window {
        position: fixed;
        background-color: rgba(255, 255, 255, 0.25);
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 999;
        visibility: hidden;
        opacity: 0;
        pointer-events: none;
        transition: all 0.3s;
    }
    .modal-window:target {
        visibility: visible;
        opacity: 1;
        pointer-events: auto;
        background: rgba(0, 0, 0, 0.5);
    }
    .modal-window > div {
        width: 700px;
        position: absolute;
        top: -1px;
        /* left: 50%; */
        height: 101vh;
        right: -1px;
        overflow-y: auto;
        /* -webkit-transform: translate(-50%, -50%); */
        /* transform: translate(-50%, -50%); */
        padding: 50px;
        border: 1px solid;
        background: #dbc4bd;
    }
    .modal-close {
        color: #000;
        line-height: 50px;
        font-size: 50px;
        position: absolute;
        right: 0;
        text-align: center;
        top: 10px;
        font-weight: 100;
        width: 70px;
        text-decoration: none;
    }
    .modal-close:hover {
        opacity: 0.5;
    }
</style>