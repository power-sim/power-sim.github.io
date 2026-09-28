# ICLR Submission 14573 — Project Page

Anonymous project page, same layout as `iclr_submission_11751` (Bulma + static HTML, no build step).
Open `index.html` directly or serve the folder with `python3 -m http.server`.

## Assets

Files already in place were copied/rendered from `figs/` and `paper_results/`; `index.html` references them.
Missing videos show a dashed "Video placeholder" box automatically and start playing once the file
lands at the listed path. All sections are filled in.

| Section | Path | Status |
|---|---|---|
| Teaser image (hero) | `new_assets/pdf_renders/teaser.png` (from `figs/teaser.pdf`) | ready |
| Why PowerSim? — figure | `new_assets/pdf_renders/evolve_sites.png` (from `figs/evolve_sites.pdf`) | ready |
| Dynamic Scene Editing with Poking — figure | `new_assets/pdf_renders/foam_edit.png` (from `figs/foam_edit.pdf`) | ready |
| Why PowerSim? | `results/why_powersim/{pac_nerf,physgaussian,powersim}.mp4` (from `paper_results/why_powersim/{pac-nerf.mp4,physgauss/output.mp4,powersim/output.mp4}`; PowerSim retimed `setpts=1.5*PTS,fps=100` from 200 to 300 frames so all three run 3 s and loop in step) | ready |
| Dynamic Scene Editing with Poking — videos | `results/poke/force_setting_{1,2,3}.mp4` (2x crop-zoom of `paper_results/bonsai_garden_poke/config{1,2,3}.mp4`: `crop=648:420:291:50`, upscaled to 1296x840; setting 2 uses `config2_fixed.mp4`, where the frame-0 force marker is held for frames 0-9 to match settings 1 and 3) | ready |
| Material Properties Estimation — images | `new_assets/material/{random,physdreamer,optimized}.png` (PhysDreamer padded from `paper_results/carnations_poke/physdreamer_mat_field_E.png` to the 380:230 panel aspect) | ready |
| Material Properties Estimation — videos | `results/material/{random,physdreamer,optimized}.mp4` (from `paper_results/carnations_poke/{unoptimized,physdreamer,optimized}.mp4`) | ready |
| More Simulation Results | `results/single_object/{pillow2sofa_drop,coke_can_compress,ficus_poke,wolf_sand,mic_drop,telephone_swing}.mp4` (from `paper_results/single_object/{pillow2sofa_drop,coke_can_compress,phase2_ficus_poke,wolf_sand_cull70,mic_lift_right_drop_white,telephone_cord_swing_ext_indicator}/output.mp4`) | ready |
| Dynamic Secondary Ray Tracing with Reflection | `results/ray_tracing/{bonsai_garden_dynamic_mirror,cafeteria}.mp4` (from `paper_results/teaser_video/bonsai_garden_dynamic_mirror/` and `paper_results/multi_physics/cafeteria/`) | ready |
| Comparison with Baselines | `results/compare/{mario,bus}.mp4` (from `paper_results/qual_dynamic_rec_compare/videos/`) | ready |
| Ablation Studies | `results/ablation/{powersim,fixed_dipole_plane,fixed_texel_axis,physgaussian}.mp4` (from `paper_results/ablation_studies/{full,fix_dipole,fix_texel_axis,physgauss}/output.mp4`) | ready |

Re-render the PDF figures with `pdftoppm -png -r 200 -singlefile figs/<name>.pdf new_assets/pdf_renders/<name>`
(then trim white margins). `paper_results/` is the raw source tree and is not referenced by the page.
