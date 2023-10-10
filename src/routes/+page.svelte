<script lang="ts">
    import PaneScrollable from "../components/PaneScrollable.svelte";
    import TextNav from "../components/text-nav/TextNav.svelte";
    import type {Destination} from "../types/NavTypes";

    let destinations: Destination[] = [
        {name: "about me", path: "#about", selected: true},
        {name: "projects", path: "#projects", selected: false},
        {name: "experience", path: "#experience", selected: false},
        {name: "contact", path: "#contact", selected: false},
        {name: "HI", path: "#hi", selected: false}
    ];
</script>

<PaneScrollable>
    <div slot="not-scrollable" class="nav">
        <TextNav destinations={destinations} />
    </div>
    <div slot="scrollable" class="body-content">
        <p class="header-text" id="about">about me</p>
        <p class="body-text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce sollicitudin ligula sit amet sagittis varius. Aenean in ultrices enim, id vehicula quam. Donec ullamcorper arcu quis convallis faucibus. Morbi mi mi, tempor gravida ornare ac, auctor et tortor. Proin ultrices at orci vel consequat. Morbi aliquet eget erat non condimentum. Phasellus vulputate, leo ac vulputate euismod, nisi felis sollicitudin justo, id blandit odio odio in ipsum. Suspendisse varius orci nec enim vehicula fringilla.
<br><br>
            Fusce nec enim et felis tincidunt interdum a vitae dolor. Ut eget ex commodo, tincidunt quam vel, venenatis purus. Donec mauris odio, tristique ac orci a, eleifend tempor ligula. Pellentesque feugiat, tortor vel varius aliquam, turpis neque auctor mi, eget mollis orci massa facilisis sem. Aliquam vel nulla efficitur, vestibulum nisi ut, posuere nisl. Nullam maximus ligula et dignissim venenatis. Nullam mollis magna ac fermentum aliquam. Integer at nisl lorem. Phasellus non tortor et velit porttitor ultrices ut ut tortor. Cras tincidunt nisi velit, sit amet rutrum nunc facilisis sed. Vivamus eget ex bibendum, molestie magna facilisis, ultrices justo. In venenatis leo at felis ultricies pulvinar. Morbi efficitur gravida leo, in accumsan metus. Phasellus id orci in justo tempor euismod sed a diam. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Suspendisse potenti.
            <br><br>
            Nulla facilisi. Curabitur finibus, nisi ac pretium maximus, dui leo tincidunt ante, in porttitor sapien dolor quis massa. Mauris ultricies scelerisque neque condimentum ultrices. Nulla facilisi. Etiam nec felis et metus viverra viverra. Curabitur diam ante, aliquet ut feugiat vel, pellentesque id leo. Phasellus et nisl a elit tristique ullamcorper. Etiam lobortis eget lacus nec pretium. Aenean laoreet erat ut nisi blandit tristique. Mauris laoreet libero eu purus pharetra venenatis. Nulla elementum elementum quam id eleifend. Nam vel eros quam. Nulla consectetur, nibh non fermentum varius, diam nunc pretium turpis, at interdum elit dui sed nibh. Integer massa risus, maximus id porta ullamcorper, tempus id magna. Proin diam ipsum, vestibulum eget velit eu, suscipit porta ligula. Sed cursus vehicula nulla, id vehicula justo dictum dictum.
            <br><br>
            Mauris non ornare dui, ut finibus quam. Aliquam congue rutrum turpis sit amet sodales. Integer vulputate scelerisque accumsan. In aliquet dignissim diam nec lacinia. Suspendisse mattis ex in diam consectetur, id placerat nulla efficitur. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed fringilla non justo eget placerat. Etiam lacinia elit augue, eget rhoncus diam egestas ut. Fusce vitae dignissim quam. Aenean nec lectus at sem vehicula malesuada. Nullam malesuada sit amet magna vitae egestas. Integer in dolor nec nunc placerat auctor. Nulla hendrerit facilisis rhoncus. In auctor risus et dolor venenatis eleifend. Maecenas eleifend urna laoreet, lacinia magna in, dapibus sem.
            <br><br>
            Vestibulum maximus ex ut purus blandit congue. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam elit urna, tempus nec vehicula eget, aliquam nec lectus. Aliquam ullamcorper dui tellus, vitae vehicula lorem viverra quis. Maecenas rhoncus aliquam quam vitae tempor. Pellentesque a nunc nec massa fringilla pellentesque et sed mi. Aliquam nunc lectus, porttitor a mattis in, suscipit luctus orci. Aliquam dignissim faucibus mi, pellentesque tempus metus vulputate quis. Praesent massa sem, bibendum sed lectus sed, rhoncus fringilla lacus. Donec turpis lorem, consequat in rutrum id, mattis at urna. Suspendisse quis accumsan libero, quis viverra augue. Aenean pulvinar hendrerit metus, sit amet fringilla nunc sagittis quis. Phasellus auctor ullamcorper ante, at molestie urna placerat sodales. In laoreet, lacus blandit commodo varius, quam orci hendrerit massa, laoreet tempus neque dui sed diam.
            <br><br>
            </p>
        <p class="header-text" id="projects">Projects</p>
        <p class="body-text">
            Aliquam ornare risus elit, nec semper tortor euismod et. Nam venenatis pulvinar lorem pulvinar eleifend. Sed ornare quis diam sit amet ultrices. Quisque arcu ante, tristique at lectus a, dapibus sodales velit. Mauris interdum ante eget purus suscipit rhoncus. Fusce ac aliquam tortor. Quisque nec pretium dui. Nam in massa leo. Duis commodo ipsum et purus mattis, vitae laoreet metus vehicula.
            <br><br>
            Aliquam dictum ullamcorper metus. Nulla vel egestas ex, vitae placerat diam. Nam fermentum diam sit amet odio sollicitudin feugiat. Vestibulum elit odio, facilisis eu placerat imperdiet, gravida at leo. Mauris placerat quam auctor tortor pulvinar pharetra. Vestibulum ut dapibus sem. In in enim leo. Nunc at vulputate velit. Sed a placerat nibh. Quisque leo mi, blandit vel sapien quis, euismod tempor ligula. Suspendisse aliquam, libero tincidunt tincidunt maximus, odio dui congue est, a mollis mauris tortor in tortor.
            <br><br>
            Mauris aliquam nunc diam, eu accumsan urna hendrerit at. Maecenas id sollicitudin turpis. Pellentesque tristique bibendum massa, et feugiat risus bibendum vitae. In volutpat, magna eget rhoncus hendrerit, dolor ligula viverra justo, consectetur volutpat nibh sapien a diam. In sollicitudin vehicula purus. Duis eu viverra enim, in maximus felis. Curabitur nec lacus a nisl mattis pulvinar. Pellentesque in turpis semper, egestas tellus eget, mattis odio. Etiam dictum, nunc sit amet imperdiet maximus, tortor ante aliquet arcu, in tristique ante elit vel libero. Nulla a risus ut erat semper iaculis vel id dolor. In vulputate magna purus, sit amet rutrum enim aliquam ut. Integer sed purus in tellus finibus placerat malesuada ac ex. Vestibulum id est ipsum. Vestibulum mollis, velit eget pretium vulputate, turpis libero sollicitudin diam, ac volutpat odio erat nec lacus. Fusce sodales cursus purus, scelerisque auctor tortor tincidunt pulvinar.
            <br><br>
            Pellentesque id molestie nisl. Phasellus condimentum feugiat semper. Pellentesque odio libero, elementum ac lacus in, mollis venenatis velit. Praesent lobortis nulla vitae lacinia suscipit. Cras eu volutpat elit. Vivamus diam urna, interdum in viverra id, faucibus sit amet metus. In a rhoncus tortor. Ut dolor ipsum, aliquam nec mattis sit amet, ultricies id sapien. Interdum et malesuada fames ac ante ipsum primis in faucibus. Curabitur sit amet ipsum vehicula, volutpat mauris sed, fringilla tortor. Aenean semper blandit pellentesque.
            <br><br>
            Donec bibendum, turpis id interdum pulvinar, nulla urna scelerisque erat, ac porta lorem nunc a orci. Cras nec felis id leo eleifend laoreet. Quisque gravida lectus accumsan sagittis blandit. Aenean finibus, sapien ut laoreet elementum, elit neque varius ipsum, eget eleifend lorem libero at turpis. Morbi ultrices ipsum nec sem congue tristique. Mauris placerat sollicitudin eros a imperdiet. Vivamus luctus metus vitae convallis lobortis. Sed vel sagittis est, pulvinar sollicitudin ex.
            <br><br>
            Praesent vulputate felis feugiat erat facilisis laoreet. Donec at tempus dolor. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Vivamus non eleifend mi. Proin ac nisi ex. Donec a aliquet sapien. Duis id magna in felis sagittis volutpat. Integer vitae odio nec neque congue egestas. Pellentesque lobortis sapien eget congue consectetur. Curabitur sed sodales nisi, in ornare turpis. Vestibulum iaculis turpis at urna accumsan, non pharetra ante rutrum. Pellentesque consectetur, magna fringilla ullamcorper accumsan, erat mauris fringilla ipsum, ac dignissim justo lacus non eros. Interdum et malesuada fames ac ante ipsum primis in faucibus. Vivamus eleifend sed ante ac interdum.
            <br><br>
            Nulla scelerisque tortor ut nulla vulputate, semper ornare turpis sollicitudin. Suspendisse faucibus viverra porta. Sed non vestibulum elit. Donec et massa sit amet nunc convallis varius nec ac urna. Donec interdum placerat varius. Praesent at dui nec dolor rhoncus laoreet quis non enim. Morbi dignissim velit sed porttitor gravida. Sed imperdiet posuere elit, vitae tincidunt nisi commodo in. Aenean ut justo nec lacus mattis egestas sit amet non nisi. Aenean tincidunt sed sapien in feugiat. Donec volutpat gravida pellentesque. Aliquam at lectus ut mi dictum cursus in a quam.
            <br><br>
            Fusce maximus nisl lacinia velit pulvinar tristique. Maecenas et dolor auctor, egestas nulla sit amet, sagittis mi. Maecenas volutpat volutpat sapien, eu rutrum ante pretium sit amet. Proin aliquet turpis rutrum odio auctor dapibus. Fusce varius sodales sapien. Phasellus sed metus vitae diam cursus vestibulum. Fusce et purus at justo mattis semper. Maecenas faucibus metus non metus molestie, vitae bibendum augue blandit. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
            <br><br>
            Etiam finibus lacus et velit convallis rhoncus. Aenean viverra id eros non gravida. Donec sed vehicula dui. Aliquam fermentum dolor vel velit mollis feugiat. Duis porttitor velit vestibulum felis interdum laoreet. Vivamus nulla nunc, auctor et lectus vitae, pellentesque porttitor lectus. Curabitur bibendum eleifend velit, vel blandit purus aliquet vel. Nulla bibendum risus at nulla lobortis, eu dignissim massa rutrum. Nulla hendrerit ornare consectetur. Suspendisse feugiat varius vehicula.
            <br><br>
            Sed finibus pretium pulvinar. Morbi ultricies lectus erat, ut tincidunt dolor lobortis quis. Donec feugiat dui magna. Maecenas dapibus nisl mauris, ac imperdiet purus pretium in. Duis pharetra elementum ligula, ut suscipit tellus commodo non. Cras vel tortor ex. Phasellus at consequat metus, nec maximus magna. Mauris eu ante luctus, pharetra justo sit amet, mollis neque. Proin pharetra dapibus ipsum consectetur tempor. Phasellus laoreet euismod velit, vitae commodo nisi faucibus at. Sed mi purus, sagittis vel auctor condimentum, ultrices non nulla. Integer in enim sed neque dignissim rhoncus. Nullam dictum nulla vitae augue aliquam, eget ornare nunc porttitor. Pellentesque lacinia semper quam, nec gravida augue tempor id. Aenean tempus faucibus laoreet. Maecenas hendrerit odio in nisi gravida, quis interdum ante condimentum.
        </p>
        <p class="header-large-text" id="hi">
            HI
        </p>
    </div>
</PaneScrollable>

<style>
    .nav {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        height: 100%;
    }

    .body-content {
        scroll-behavior: smooth;
    }
</style>
