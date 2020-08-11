<script>
  import RotatingImages from "../components/RotatingImages.svelte";

  let width = 0;

  function setImages() {
    if (width) {
      return [
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/storefront2_xgkol6.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/peters-bakery_2_cptcp3.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/storefront_gfnhaa.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/store_rz5yik.jpg"
        }
      ];
    } else {
      return [
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/storefront2_xgkol6.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/peters-bakery_2_cptcp3.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/storefront_gfnhaa.jpg"
        },
        {
          src:
            "https://res.cloudinary.com/tihos/image/upload/c_fill,g_auto,h_500,w_2800/b_rgb:020202,e_gradient_fade,y_0.40/c_scale,co_rgb:ffffff,fl_relative,w_0.5,y_0.18/v1596475793/peters-bakery/store_rz5yik.jpg"
        }
      ];
    }
  }
  let images = setImages();
</script>

<style>
  header {
    position: relative;
    height: 350px;
    overflow: hidden;
    border-bottom: 5px solid var(--gold);
  }
  @media (max-width: 1000px) {
    header {
      border-bottom: 4px solid var(--gold) !important;
    }
  }
</style>

<svelte:window bind:innerWidth={width} />
<header>
  <RotatingImages {images} speed={3000} />
</header>
