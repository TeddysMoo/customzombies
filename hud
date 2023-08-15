<div align="center">
<img alt="Zombies" src="https://lh3.googleusercontent.com/fife/AKsag4MtN5PE25MpupPa8Kils7FWuxh-EcezPOeRrpsg91R8F2dVa9swrqgcc9N5sOwCZskkOWY78MN5FoYTVNl-g8F8J9RKWnL2cJJiZslmb3TTrvsFkVWbzUgS-K4cFTLgpCZgIzjLYsz9PdxufSdTbr8sicsVjBh2KPjyaCEDfGJrNZ6u79_pPp0sKqvpkJudU-7sVmnN-nZwtZGKLGi2PHhbxLxglN0PATik1qBBR0nZVDlyq775G1LLh-h9TKH25BY3fgkJPUuc3kEsMrSuJEQEio37aCkWJDYvGSUCN_TedEplTmtP9XyvW_vmuHcV49zK_jf8FXfCunckPJJjw4XgWO_sxloFOWgL81iw_T8NVOD5mN15StH5Zed8lHWMgrYpL18ISDdD06bgyRBQwlyvpQDpspc_nv64UZVghUZeyNXA8C2OAVaAYwfu2SHjswzdzI9SWRQ_8EJs8Upd4jlIYftyHFmDu6-BoDaAbKoZz_9aMu6vNytd8ZINsRa6j7eLZdpphlGjCSLausZYwOWFeMNVMvFSBNpLlxFAl2ih6IfmtSzK4MKbvveLRovHwaWQhKKDpiNuxAsfwz0r0wkkcIav0J7MF5o3QN8fIQ9a8DIil6uP82MG4sbiwVvY7yctfcYIh9-966-bngNABMkD6pZgvb99NkK34Xdq1oKhfec_zXEkyiUEnjaw1jXSKR-XyqnnpwQ3uujvd07seYNbAHBz94UBuV0GpKgZeJT9HVI9eken5TD3oLccOAM8RDcs5-cowDUjQ8J-X_SY_kgc-ss33LXvV7f709BI4Dwqyi-mWRqaxVXbckEghfHRMD_N0wJ9BI8Im5ABhx9ZJWBRYiIWMV9lMtiZU1NV51XiOerRUdhfaQJHIT8n7JnYr35sEnpPciUO-GBPsHyXZLNFlg8UVGDZRfMHv-MDlLVrt53PkE9JQufTFi8aqHtV-oRGibElHr97VdU3eSHN6Exd7t5CLNPRzGScKTQum9G1eN2rXU5v9yfEdO30_SJCKBCXsAiHyut1Z1z0JaFSRqQGim-UK9WoiLivvspbhmQXEHFJnh7Z-c9HTWrOS10PzEN8BYYJ5zASH5p3Yw44Zx7YzN-xqr_fkXulLYZiukSMb_JgGSUazzmUAFWLz_qBGSS8un7eUw_I3uLusuof3fin-7T9tI3Dh5p-yuxw5is2VfQL4ZXNlEYJ_rzrV4uSyp0ETIMvAWs3CCumhO2tG2L9uAHX1XI_AGBE6HLpsVGSXc_LcyTbji6zKJ0WFC6p7GAAla77LVAzg7Uw6cUhUgJQAO90hOVEtlTC7OJyvGou6pcX2QKgtTXCUwBkOVBAxre5fXM12iMyzRi1vwserCIqBn8HD0kLnxAplarX5h4rIeOG1Jey6qXEVRsB-eOgMzbdRnZJnDhUyvQuukLfJGxjfG2mugKLWNFcOjsGaZUYlp1TyotLvRbimdQYkykRE3Ztpx6mn3Om_0iowHfY4Dlh65P7umMFn5zU-Q1UPevUIh_fH3X7Px56S7yPy5Rw2wu2MA=w2560-h1315">
<h1> 🧟‍♂️ HUD Mods </h1>
</div>

## 🔫 Typewriter Text Intro
  
  Navagate to: <b>`usermaps/scrips/zm/usermap.gsc`</b> and add the following line to <b>`main();`</b>:
  
  ```bash
  level thread intro_screen_text();
  ```

  Then add the following lines to the bottom of <b>`mapname.gsc`</b>:

  ```bash
    
  function intro_screen_text()
{
    wait(1); // wait for flags to init
    level flag::wait_till("initial_blackscreen_passed");

    intro_hud = [];
    str_text = Array( "line_one_text", "line_two_text", "line_three_text" ); // Edit these lines to say what you want

    for ( i = 0; i < str_text.size; i++ )
    {
        intro_hud[i] = NewHudElem();
        intro_hud[i].x = 20;
        intro_hud[i].y = -250 + ( 20 * i );
        intro_hud[i].fontscale = ( IsSplitScreen() ? 2.75 : 1.75 );
        intro_hud[i].alignx = "LEFT";
        intro_hud[i].aligny = "BOTTOM";
        intro_hud[i].horzalign = "LEFT";
        intro_hud[i].vertalign = "BOTTOM";
        intro_hud[i].color = (1.0, 1.0, 1.0);
        intro_hud[i].alpha = 1;
        intro_hud[i].sort = 0;
        intro_hud[i].foreground = true;
        intro_hud[i].hidewheninmenu = true;
        intro_hud[i].archived = false;
        intro_hud[i].showplayerteamhudelemtospectator = true;
        intro_hud[i] SetText(str_text[i]);
        intro_hud[i] SetTypewriterFX( 100, 10000 - ( 3000 * i ), 3000 );
        wait(3);
    }

    wait(10);
    foreach ( hudelem in intro_hud ) hudelem Destroy();
}

  ```
