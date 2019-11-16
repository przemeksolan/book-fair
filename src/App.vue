<template>
    <div class="app">
        <main class="pa-h_l ma-b_l">

            <header class="flex wrap-no gap_xs ma-t_m">
                <div class="span-auto">
                    <a href="/" class="pa_s pa-l_l block bo-t_px bo-r_px bo-b_px text-bold docs-teutonic-link">
                        <div class="muted">Organized by the</div> Enterprise Ireland <div class="muted">&</div> Higher Education Ireland
                    </a>
                </div>
                <div class="span-auto hide-p">
                    <div class="search-box docs-search" id="app">
                        <span class="algolia-autocomplete" style="position: relative; display: inline-block; direction: ltr;">
                            <input tabindex="1" v-model="search" type="search" class="clicker input algoliaSearch ds-input" placeholder="Search by title, genre or author" size="30" autocomplete="off" spellcheck="false" role="combobox" aria-autocomplete="list" aria-expanded="false" aria-label="search input" aria-owns="algolia-autocomplete-listbox-0" dir="auto" style="position: relative; vertical-align: top;">
                            <div class="search-results">
                                <ul class="gap_no ma-t_xs">
                                    <li v-for="post in filteredList" v-bind:key="post">
                                        <a class="block-link bo-t_px" v-bind:href="post.link" target="_blank">
                                            {{ post.title }}<small> by {{ post.author }}</small>
                                        </a>

                                    </li>
                                </ul>
                            </div>
                        </span>
                    </div>
                </div>
                <div class="span-auto ma-l-auto ma-t_s">
                    <a href="#visitors" class="ma-r_l">Visitors</a>
                    <a href="#exhibitors" class="ma-r_l">Exhibitors</a>
                    <a href="#about" class="ma-r_l ">About</a>
                    <a href="#subscribe">Get Updates</a>
                </div>

                <div id="subscribe" class="modal-window">
                    <div>
                        <a href="#" title="Close" class="modal-close">&#215;</a>
                        <div class="flex wrap-no ma-b_s">
                            <h2 id="form-error">Know what’s now.</h2>
                        </div>
                        <div class="text_l read_l">
                            <p>Sign up for the newsletter to keep up with us.</p>
                        </div>
                        <form class="gap-no ma-t_l">
                            <div class="form-box">
                                <label for="email" class="mini-label">Enter your e-mail</label>
                                <input type="email" id="email" name="email" class="input" placeholder="your@email.com" required="">
                            </div>
                            <div class="form-box danger">
                                <label for="password" class="mini-label">Choose a safe password</label>
                                <input type="password" id="password" name="password" class="input" placeholder="••••••••" required="" min="8">
                            </div>
                            <label class="box">
                                <input type="checkbox" id="terms" name="terms" class="checkbox" required="">
                                Accept the <a href="#" class="link">terms and conditions</a>
                            </label>
                            <button class="button block prime" type="submit">Sign up →</button>
                        </form>

                        <div class="flex wrap-no ma-b_m ma-t_l">
                            <h3>
                                Share Us
                            </h3>
                        </div>
                        <div class="grid gap_s">
                            <div class="span-1 span-2-t span-3-p">
                                <a href="https://facebook.com"><img class="ar-1-1 ra-circle media" src="https://facebookbrand.com/wp-content/uploads/2019/04/f_logo_RGB-Hex-Blue_512.png" alt="Photo via adorable.io/avatars"></a>
                            </div>
                            <div class="span-1 span-2-t span-3-p">
                                <a href="https://twitter.com"><img class="ar-1-1 ra-circle " src="https://www.stickpng.com/assets/images/5a2fe3efcc45e43754640848.png" alt="Photo via adorable.io/avatars"></a>
                            </div>
                            <div class="span-1 span-2-t span-3-p">
                                <a href="https://youtube.com"><img class="ar-1-1 ra-circle " src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/YouTube_social_white_circle_%282017%29.svg/1024px-YouTube_social_white_circle_%282017%29.svg.png" alt="Photo via adorable.io/avatars"></a>
                            </div>
                        </div>
                    </div>
                </div>
            </header>

            <!-- About Section -->
            <section class="ma-t_m pa-t_l full-height">
                <h1 class="text-hero_l pa-t_l ma-t_l text-sans text-black read_xxl">Cork Book Fair</h1>
                <div class="text_xl text-sans read_xl ma-t_m">
                    <p>An international book fair selling and exhibiting books, printed matter, stationary, printing, compact discs and other multimedia publishing.</p>
                </div>
            </section>

            <footer class="pa-v_m text_s span-auto ma-t_l pa-b_l">
                <nav class="flex">
                    <div>
                        <b>August</b> 14 - 16<br>
                        at <a href="https://twitter.com/frank_laemmer" class="link">Pairc Ui Chaoimh</a> & <a class="fortrabbit link" href="https://www.fortrabbit.com">Cork City Hall</a><br>
                    </div>
                    <div class="ma-l-auto span-auto flex-end" style="margin-top: -20px;">
                        <a href="#tickets" class="button prime dis-b text_l pa_m block">Buy Tickets</a>
                    </div>
                </nav>
            </footer>

            <div id="tickets" class="modal-window">
                <div>
                    <a href="#" title="Close" class="modal-close">&#215;</a>
                    <div class="flex wrap-no ma-b_s">
                        <h2>Admission</h2>
                    </div>
                    <div class="text_l read_l">
                        <p>Reserve your place today</p>
                    </div>
                    <form class="gap-no ma-t_l">

                        <div class="form-box pa_m">
                            <label for="email" class="mini-label required">Name on card</label>
                            <input type="text" class="input" id="cardholder" name="cardholder" required="">
                            <div class="mini-info">Exact name as shown on card</div>
                        </div>
                        <div class="flex gap-no">
                            <div class="form-box pa_m">
                                <label for="card_expire_month" class="required mini-label">Expire month</label>
                                <select id="card_expire_month" name="card_expire_month" class="select">
                                    <option disabled="" selected="">MM</option>
                                    <option value="01">01</option>
                                    <option value="01">02</option>
                                    <option value="01">03</option>
                                    <option value="04">04</option>
                                    <option value="05">05</option>
                                    <option value="06">06</option>
                                    <option value="07">07</option>
                                    <option value="08">08</option>
                                    <option value="09">09</option>
                                    <option value="10">10</option>
                                    <option value="11">11</option>
                                    <option value="12">12</option>
                                </select>
                            </div>
                            <div class="form-box pa_m">
                                <label for="card_expire_month" class="required mini-label">Expire year</label>
                                <select id="card_expire_year" name="card_expire_year" class="select">
                                    <option disabled="" selected="">YYYY</option>
                                    <option value="2017">2017</option>
                                    <option value="2018">2018</option>
                                    <option value="2019">2019</option>
                                    <option value="2020">2020</option>
                                    <option value="2021">2021</option>
                                    <option value="2022">2022</option>
                                    <option value="2023">2023</option>
                                </select>
                            </div>
                        </div>
                        <div class="flex wrap-no gap-no">
                            <div class="form-box pa_m">
                                <label for="card_number" class="mini-label required">Card number</label>
                                <input type="text" id="card_number" name="card_number" class="input" maxlength="16" placeholder="4916800099659557" required="">
                            </div>
                            <div class="form-box pa_m span-third">
                                <label for="card_cvv" class="mini-label required">Security Code</label>
                                <input type="text" id="card_cvv" name="card_cvv" class="input" maxlength="4" placeholder="123" required="">
                                <div class="mini-info">3-4 digits</div>
                            </div>
                        </div>
                        <button class="button prime dis-b text_l pa_m block" type="submit">Save</button>
                        <p class="text_s ma-t_s">
                            Pisa, Vastercard &amp; Emerican Axpress are accepted.
                        </p>
                    </form>
                </div>
            </div>

            <!-- Exhibitors Section -->
            <h2 id="visitors" class="bo-b_xs pa-b_xs ma-t_l pa-t_l">Exhibitors</h2>
            <div class="columns gap-no cols-4 cols-2-t collapse-p">
                <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">
                    <div class="span-auto pa-l_xs">
                        <div class="bg-a flex ra-circle bo_px width_l height_l">
                            <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">C</div>
                        </div>
                    </div>
                    <div class="ma-l_s text-clip flex">
                        <a href="#cambridge" class="span-auto self-center">Cambridge University Press</a>
                    </div>
                </div>
                <div id="cambridge" class="modal-window">
                    <div>
                        <a href="#" title="Close" class="modal-close">&#215;</a>
                        <figure class="ar-16-9 media bo_px ma-b_m"><img src="https://miro.medium.com/max/2625/1*YiY1yK5GBk4wJzTasm5MqA.jpeg" alt="Photo via picsum.photos"></figure>
                        <h1>Cambridge University Press</h1>
                        <div class="ma-b_xs ma-t_s">
                            Booth Number -
                            <span style="text-decoration: underline">A12</span>
                        </div>
                        <div class="ma-b_xs ma-t_s">
                            <a href="https://www.cambridge.org" style="text-decoration: underline">https://www.cambridge.org</a>
                        </div>
                        <div class="text_l read_l ma-t_m">
                            <p>Cambridge University Press is a department of the University of Cambridge and is both an academic and educational publisher.</p>
                        </div>
                        <div class="read_l ma-t_l">
                            <h3 id="">Recommended Books</h3>
                            <ul class="gap_no ma-t_xs bo-t_xs">
                                <li v-for="post in filteredList" v-bind:key="post">
                                    <a href="#" class="block-link bo-t_px">{{ post.title }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">
                    <div class="span-auto pa-l_xs">
                        <div class="bg-a flex ra-circle bo_px width_l height_l">
                            <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">O</div>
                        </div>
                    </div>
                    <div class="ma-l_s text-clip flex">
                        <a href="#oxford" class="span-auto self-center">Oxford University Press</a>
                    </div>
                </div>
                <div id="oxford" class="modal-window">
                    <div>
                        <a href="#" title="Close" class="modal-close">&#215;</a>
                        <figure class="ar-16-9 media bo_px ma-b_m"><img src="https://upload.wikimedia.org/wikipedia/commons/0/0c/Oxford_University_Press_from_Somerville_College.jpg" alt="Photo via picsum.photos"></figure>
                        <h1>Oxford University Press</h1>
                        <div class="ma-b_xs ma-t_s">
                            Booth Number -
                            <span style="text-decoration: underline">B45</span>
                        </div>
                        <div class="ma-b_xs ma-t_s">
                            <a href="http://global.oup.com" style="text-decoration: underline">http://global.oup.com</a>
                        </div>
                        <div class="text_l read_l ma-t_m">
                            <p>The largest university press in the world, and the second oldest after Cambridge University Press. It is a department of the University of Oxford </p>
                        </div>
                        <div class="read_l ma-t_l">
                            <h3>Recommended Books</h3>
                            <ul class="gap_no ma-t_xs bo-t_xs">
                                <li v-for="post in filteredList" v-bind:key="post">
                                    <a href="#" class="block-link bo-t_px">{{ post.title }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">
                    <div class="span-auto pa-l_xs">
                        <div class="bg-a flex ra-circle bo_px width_l height_l">
                            <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">H</div>
                        </div>
                    </div>
                    <div class="ma-l_s text-clip flex">
                        <a href="#harvard" class="span-auto self-center">Harvard University Press</a>
                    </div>
                </div>
                <div id="harvard" class="modal-window">
                    <div>
                        <a href="#" title="Close" class="modal-close">&#215;</a>
                        <figure class="ar-16-9 media bo_px ma-b_m"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Kittredge_Hall_-_Harvard_University_-_DSC01440.jpg/2560px-Kittredge_Hall_-_Harvard_University_-_DSC01440.jpg" alt="Photo via picsum.photos"></figure>
                        <h1>Harvard University Press</h1>
                        <div class="ma-b_xs ma-t_s">
                            Booth Number -
                            <span style="text-decoration: underline">C32</span>
                        </div>
                        <div class="ma-b_xs ma-t_s">
                            <a href="https://www.hup.harvard.edu" style="text-decoration: underline">www.hup.harvard.edu</a>
                        </div>
                        <div class="text_l read_l ma-t_m">
                            <p>A publishing house established on January 13, 1913, as a division of Harvard University, and focused on academic publishing.</p>
                        </div>
                        <div class="read_l ma-t_l">
                            <h3>Recommended Books</h3>
                            <ul class="gap_no ma-t_xs bo-t_xs">
                                <li v-for="post in filteredList" v-bind:key="post">
                                    <a href="#" class="block-link bo-t_px">{{ post.title }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="flex wrap-no ma-b_xs pa-v_s bo-t_px">
                    <div class="span-auto pa-l_xs">
                        <div class="bg-a flex ra-circle bo_px width_l height_l">
                            <div class="span-auto self-center ma-h-auto type_s text-serif text-bold text_xl">C</div>
                        </div>
                    </div>
                    <div class="ma-l_s text-clip flex">
                        <a href="#cork" class="span-auto self-center">Cork University Press</a>
                    </div>
                </div>
                <div id="cork" class="modal-window">
                    <div>
                        <a href="#" title="Close" class="modal-close">&#215;</a>
                        <figure class="ar-16-9 media bo_px ma-b_m"><img src="https://rm-content.s3.amazonaws.com/56042efc0266cb307da087e0/409210/upload-6743c3e0-6361-11e5-8eb9-bd1ef5c052bd.jpg" alt="Photo via picsum.photos"></figure>
                        <h1>Cork University Press</h1>
                        <div class="ma-b_xs ma-t_s">
                            Booth Number -
                            <span style="text-decoration: underline">G05</span>
                        </div>
                        <div class="ma-b_xs ma-t_s">
                            <a href="http://www.corkuniversitypress.com/" style="text-decoration: underline">http://www.corkuniversitypress.com/</a>
                        </div>
                        <div class="text_l read_l ma-t_m">
                            <p>A publisher located in Cork, Ireland. It was founded in 1925 and is associated with University College Cork.</p>
                        </div>
                        <div class="read_l ma-t_l">
                            <h3 id="">Recommended Books</h3>
                            <ul class="gap_no ma-t_xs bo-t_xs">
                                <li v-for="post in filteredList" v-bind:key="post">
                                    <a href="#" class="block-link bo-t_px">{{ post.title }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

            <div class="docs-example docs-standard-table ma-h_l-">
                <div class="ma-t_l pa-h_l pa-v_l">
                    <h2 id="syntax-highlighting">Rules and Regulations</h2>
                    <div class="ma-t_s">
                        <p class="text_l">Your registration for the Exhibition, or entry to our exhibition venue, signifies your acceptance of these Rules and Regulations and any other rules and regulations referenced herein or reasonably notified to you at the Exhibition venue, with which you agree to observe and comply.
                            Visitors do not have the Organizer’s permission to attend, and may not attend, the Exhibition without confirming your acceptance of these Rules and Regulations in writing prior to your attendance. Your admission badge allows you entrance to concurrent Exhibitions organized by the government with other event partners. By doing so, you accept and agree to abide by the Visitor’s Rules & Regulations of respective Exhibition.

                        <p class="ma-t_s">1. Visitor’s Conduct: You shall not do or permit to be done any action which causes or may cause any disturbance, nuisance, annoyance, inconvenience, damage or danger to any person or thing or
                            Page 1 / 4
                            which in the opinion of the Organizer does not conform to the general standards of the Exhibition or constitutes a breach of these Rules and Regulations.
                            We reserve the right to refuse admittance to any visitor or to require any visitor to leave if their behavior is in breach of these Rules and Regulations, or contravenes applicable laws or regulations. Our opinion is final in this regard.</p>
                        <p class="ma-t_s">2. Liability: We shall not be liable for any loss of or damage to any of your property occurring in or about the Exhibition venue, or for the death of or any injury sustained by any visitor whilst in or about the Exhibition venue, other than for death or injury resulting from our negligence or which otherwise cannot be excluded or restricted at law.
                            You agree that we shall not incur any liability to you for any goods or services offered or sold by, or representations made by, any Exhibitor at the Exhibition.
                            You agree to indemnify and hold us harmless against any damage or allegations of damage caused by you to the property, business or reputation of us, other Exhibitors or Visitors or the operator of the Exhibition venue, including but not limited to damages arising from your breach of these Rules and Regulations.
                            You agree that we shall not incur any liability to you for any error or omission in any informa- tion relating to any Exhibitor or its products in the Exhibition’s official directory or in any other promotional or other printed materials or information provided by us or that Exhibitor.</p>
                        <p class="ma-t_s">3. Recording: You shall not record images in any form while attending the Exhibition without our prior written consent. Such prohibition includes, but is not limited to, the taking of photographs, video or digital recording of any type and drawing or sketching of images. You agree to surrender to us on demand whatever media on which images may be recorded in violation of this rule.
                            The copyright and other intellectual property or other rights (including for the avoidance of doubt, rights in sound recording and broadcasts) in materials created in violation of this clause 4, whether arising now or in the future, shall belong to us unconditionally from the time of their creation, and you agree to do all acts and execute all such documents as may be required to properly vest the same.
                            You agree to indemnify and hold us harmless against all claims, liabilities, losses, proceedings, damages, judgments, expenses, costs (including legal fees) and charges of any kind howsoever incurred by or on behalf of or made against us arising out of any infringement or other claim relating to or arising out of the unauthorized making of any recordings by you.
                            You acknowledge and agree that we may take photographs/videos which could include images of you while attending the Exhibition. You hereby consent to and grant to us, the unrestricted, perpetual, worldwide, royalty-free and transferable right and license to use such images worldwide without any compensation. You acknowledge that we are the exclusive owner of all rights in such images and hereby waive (a) any and all rights in and to them, and (b) any and all claims you may have relating to or arising from our use of them.</p>
                    </div>
                </div>
            </div>




<!--            &lt;!&ndash; Tickets Section &ndash;&gt;-->
<!--            <h1 id="exhibitors" class="ma-t_l ma-b_m text-hero_m">Register</h1>-->
<!--            <p class="text_l ma-b_m">Register your details below to be involved</p>-->
<!--        §x§    <Tickets />-->

            <article>
                <header class="ma-t_l ma-b_s">
                    <div id="exhibitors" class="flex wrap-no ma-b_s">
                        <h2 id="invalid-input">
                            Participate
                        </h2>
                    </div>
                    <div class="text_l read_l">
                        <p>Register and Pay for the Participation</p>
                    </div>
                    <div class="ma-v_m">
                        <div>
                            <b>The Price</b>:
                            <code class="ma-r_xs"><a href="https://github.com/fortrabbit/teutonic-css/blob/master/includes/_forms.scss" class="link">€235</a></code>
                        </div>
                    </div>
                    <form class="gap-no read_m ma-v_s ma-v_l">
                        <h4 class="bo-b_xs pa-b_xs">
                            Credit card details
                        </h4>
                        <div class="form-box pa_m">
                            <label for="email" class="mini-label required">Name on card</label>
                            <input type="text" class="input" id="cardholder" name="cardholder" required="">
                            <div class="mini-info">Exact name as shown on card</div>
                        </div>
                        <div class="flex gap-no">
                            <div class="form-box pa_m">
                                <label for="card_expire_month" class="required mini-label">Expire month</label>
                                <select id="card_expire_month" name="card_expire_month" class="select">
                                    <option disabled="" selected="">MM</option>
                                    <option value="01">01</option>
                                    <option value="01">02</option>
                                    <option value="01">03</option>
                                    <option value="04">04</option>
                                    <option value="05">05</option>
                                    <option value="06">06</option>
                                    <option value="07">07</option>
                                    <option value="08">08</option>
                                    <option value="09">09</option>
                                    <option value="10">10</option>
                                    <option value="11">11</option>
                                    <option value="12">12</option>
                                </select>
                            </div>
                            <div class="form-box pa_m">
                                <label for="card_expire_month" class="required mini-label">Expire year</label>
                                <select id="card_expire_year" name="card_expire_year" class="select">
                                    <option disabled="" selected="">YYYY</option>
                                    <option value="2017">2017</option>
                                    <option value="2018">2018</option>
                                    <option value="2019">2019</option>
                                    <option value="2020">2020</option>
                                    <option value="2021">2021</option>
                                    <option value="2022">2022</option>
                                    <option value="2023">2023</option>
                                </select>
                            </div>
                        </div>
                        <div class="flex wrap-no gap-no">
                            <div class="form-box pa_m">
                                <label for="card_number" class="mini-label required">Card number</label>
                                <input type="text" id="card_number" name="card_number" class="input" maxlength="16" placeholder="4916800099659557" required="">
                            </div>
                            <div class="form-box pa_m span-third">
                                <label for="card_cvv" class="mini-label required">Security Code</label>
                                <input type="text" id="card_cvv" name="card_cvv" class="input" maxlength="4" placeholder="123" required="">
                                <div class="mini-info">3-4 digits</div>
                            </div>
                        </div>
                        <button class="button prime dis-b text_l pa_m block" type="submit">Save</button>
                        <p class="text_s ma-t_s">
                            Pisa, Vastercard &amp; Emerican Axpress are accepted.
                        </p>
                    </form>

                </header>

                <div class="docs-example docs-credit-card-form ma-h_l- pa-h_l pa-v_l">


                </div>

            </article>

            <header class="ma-b_s">
                <div class="flex wrap-no ma-b_l">
                    <h2>Renowned Writers</h2>
                </div>
            </header>
            <div class="docs-profile-container grid-auto gap_s">
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&1" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/1.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Jessica Joe</h3>
                            <p class="ma-t_xs">Bald. Often Unreliable. Easily distracte.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">83</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">123</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">343</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&asd" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/2.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Manual Man</h3>
                            <p class="ma-t_xs">A human. Being.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">69</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">89</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">320</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&22" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/3.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Johannes Jan</h3>
                            <p class="ma-t_xs">Born at a very young age.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">176</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">123</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">343</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&vvv" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/4.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Franky Free</h3>
                            <p class="ma-t_xs">Insert pretentious crap about myself here.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">119</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">37</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">243</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&zzzz" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/5.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Angie Ace</h3>
                            <p class="ma-t_xs">I’m really a giant cupcake. Afraid of roller coasters and dry ice.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">117</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">102</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">282</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex column bo_px docs-profile ra_s bs_xs">
                    <div class="span-auto cover media ar-16-9 ra-t_s tinted-bg-warn">
                        <img src="//picsum.photos/300/200/?random&gg" alt="">
                    </div>
                    <div class="pa-h_m zi-1">
                        <div class="text-center ma-b_m">
                            <img src="//randomuser.me/api/portraits/lego/6.jpg" alt="Portrait" class="ra-circle ma-t_l- bo_xs">
                            <h3 class="text-clip">Judy Jane</h3>
                            <p class="ma-t_xs">I’m not smart. I just wear glasses.</p>
                        </div>
                    </div>
                    <div class="span-auto ma-t-auto pa-v_m bg-warn-2 ra-b_s">
                        <div class="flex wrap-no">
                            <div class="span-third text-center">
                                <b class="block">70</b>
                                <span class="text_s block">Photos</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">89</b>
                                <span class="text_s block">Followers</span>
                            </div>
                            <div class="span-third text-center">
                                <b class="block">92</b>
                                <span class="text_s block">Likes</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
<!--            &lt;!&ndash; Venue Section &ndash;&gt;-->
<!--            <h1 id="about" class="ma-t_l ma-b_m text-hero_m" style="margin-top: 200px;">Venue</h1>-->
<!--            <Venue />-->

<!--            &lt;!&ndash; Art Gallery Section &ndash;&gt;-->
<!--            <h1 id="art" class="ma-t_l ma-b_m text-hero_l" style="margin-top: 200px;">Gallery</h1>-->
<!--            <Art />-->

        </main>
    </div>



    <!--  <div id="app">-->
    <!--    <img alt="Vue logo" src="./assets/logo.png">-->
    <!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <!--  </div>-->
</template>

<script>
    import Tickets from './components/Tickets.vue';
    import Exhibitors from "./components/Exhibitors";
    import Venue from "./components/Venue";
    import Art from "./components/Art";

    export default {
        name: 'app',
        components: {
            Tickets,
            Exhibitors,
            Venue,
            Art
        },
        el: '#app',
        data: function() {
            return {
                search: '',
                postList: [
                    new Post(
                        'The Lord of the Rings',
                        '#',
                        'J.R.R. Tolkien'
                    ),
                    new Post(
                        'Hamlet',
                        '#',
                        'William Shakespeare'
                    ),
                    new Post(
                        'The Shining',
                        '#',
                        'Stephen King'
                    ),
                    new Post(
                        'Ulysses',
                        '#',
                        'James Joyce'
                    ),
                    new Post(
                        'The Chronicles of Narnia',
                        '#',
                        'C.S. Lewis'
                    ),
                    new Post(
                        'De Profundis',
                        '#',
                        'Oscar Wilde'
                    ),
                    new Post(
                        'Les Misérables',
                        '#',
                        'Victor Hugo'
                    ),
                    new Post(
                        'Divine Comedy',
                        '#',
                        'Divine Comedy'
                    ),
                ]
            };
        },
        computed: {
            filteredList() {
                return this.postList.filter(post => {
                    return post.title.toLowerCase().includes(this.search.toLowerCase())
                })
            }
        }
    }

    class Post {
        constructor(title, link, author, img) {
            this.title = title;
            this.link = link;
            this.author = author;
            this.img = img;
        }
    }


</script>

<style>
    html { scroll-behavior: smooth; }
    .docs-profile-container  { --grid-auto-min: 14rem;  }
    .docs-profile img {  width:8rem; }

    .muted {
        color: #999999;
        display: inline;
        font-weight: 300;
    }
    .wrapper {
        display: flex;
        max-width: 444px;
        flex-wrap: wrap;
        padding-top: 12px;
    }

    .card {
        box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
        max-width: 124px;
        margin: 12px;
        transition: .15s all ease-in-out;
    }
    .card:hover {
         transform: scale(1.1);
     }


    .search-results {
        display: none;
        background-color: #dbd6f5;
        position: absolute;
        padding: 15px;
        width: 454px;
        border: 1px solid #000;
    }

    .clicker:focus + .search-results {
        display:block;
    }

    .full-height {
        height: 65vh;
    }
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
        right: -6px;
        text-align: center;
        top: 0;
        font-weight: 100;
        width: 70px;
        text-decoration: none;
    }
    .modal-close:hover {
        opacity: 0.5;
    }

    .docs-example:before, .docs-example:after {
        content: '';
        position: absolute;
        width: 100%;
        left: 0;
        z-index: 10;
        border-top: calc(var(--space-px) * 2) dashed var(--color-main-3);
    }
</style>
