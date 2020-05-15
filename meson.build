project(
    'Quake-2',
    'c',
    default_options: [
        'warning_level=3',
        'c_std=c11'
    ]
)

cc = meson.get_compiler('c')

libdl_dep = cc.find_library('dl')
libm_dep = cc.find_library('m')
libx11_dep = dependency('x11')
libxext_dep = dependency('xext')
xxf86dga_dep = dependency('xxf86dga')
xxf86vm_dep = dependency('xxf86vm')

#
# Quake 2 engine
#

sources = [
    'client/cl_cin.c',
    'client/cl_ents.c',
    'client/cl_fx.c',
    'client/cl_input.c',
    'client/cl_inv.c',
    'client/cl_main.c',
    'client/cl_newfx.c',
    'client/cl_parse.c',
    'client/cl_pred.c',
    'client/cl_scrn.c',
    'client/cl_tent.c',
    'client/cl_view.c',
    'client/console.c',
    'client/keys.c',
    'client/menu.c',
    'client/qmenu.c',
    'client/snd_dma.c',
    'client/snd_mem.c',
    'client/snd_mix.c',
    'game/m_flash.c',
    'game/q_shared.c',
    'linux/cd_linux.c',
    'linux/glob.c',
    'linux/net_udp.c',
    'linux/q_shlinux.c',
    'linux/snd_linux.c',
    'linux/sys_linux.c',
    'linux/vid_menu.c',
    'linux/vid_so.c',
    'qcommon/cmd.c',
    'qcommon/cmodel.c',
    'qcommon/common.c',
    'qcommon/crc.c',
    'qcommon/cvar.c',
    'qcommon/files.c',
    'qcommon/md4.c',
    'qcommon/net_chan.c',
    'qcommon/pmove.c',
    'server/sv_ccmds.c',
    'server/sv_ents.c',
    'server/sv_game.c',
    'server/sv_init.c',
    'server/sv_main.c',
    'server/sv_send.c',
    'server/sv_user.c',
    'server/sv_world.c'
]

deps = [
    libdl_dep,
    libm_dep
]

executable(
    'quake2',
    sources,
    dependencies: deps,
    install: true
)

#
# Quake 2 game library
#

sources = [
    'game/g_ai.c',
    'game/g_chase.c',
    'game/g_cmds.c',
    'game/g_combat.c',
    'game/g_func.c',
    'game/g_items.c',
    'game/g_main.c',
    'game/g_misc.c',
    'game/g_monster.c',
    'game/g_phys.c',
    'game/g_save.c',
    'game/g_spawn.c',
    'game/g_svcmds.c',
    'game/g_target.c',
    'game/g_trigger.c',
    'game/g_turret.c',
    'game/g_utils.c',
    'game/g_weapon.c',
    'game/m_actor.c',
    'game/m_berserk.c',
    'game/m_boss2.c',
    'game/m_boss3.c',
    'game/m_boss31.c',
    'game/m_boss32.c',
    'game/m_brain.c',
    'game/m_chick.c',
    'game/m_flash.c',
    'game/m_flipper.c',
    'game/m_float.c',
    'game/m_flyer.c',
    'game/m_gladiator.c',
    'game/m_gunner.c',
    'game/m_hover.c',
    'game/m_infantry.c',
    'game/m_insane.c',
    'game/m_medic.c',
    'game/m_move.c',
    'game/m_mutant.c',
    'game/m_parasite.c',
    'game/m_soldier.c',
    'game/m_supertank.c',
    'game/m_tank.c',
    'game/p_client.c',
    'game/p_hud.c',
    'game/p_trail.c',
    'game/p_view.c',
    'game/p_weapon.c',
    'game/q_shared.c'
]

deps = [
    libm_dep
]

library(
    'gamex86_64',
    sources,
    name_prefix: '',
    dependencies: deps,
    install: true
)

#
# Quake 2 engine software renderer
#

sources = [
    'game/q_shared.c',
    'linux/glob.c',
    'linux/q_shlinux.c',
    'linux/rw_x11.c',
    'ref_soft/r_aclip.c',
    'ref_soft/r_alias.c',
    'ref_soft/r_bsp.c',
    'ref_soft/r_draw.c',
    'ref_soft/r_edge.c',
    'ref_soft/r_image.c',
    'ref_soft/r_light.c',
    'ref_soft/r_main.c',
    'ref_soft/r_misc.c',
    'ref_soft/r_model.c',
    'ref_soft/r_part.c',
    'ref_soft/r_poly.c',
    'ref_soft/r_polyse.c',
    'ref_soft/r_rast.c',
    'ref_soft/r_scan.c',
    'ref_soft/r_sprite.c',
    'ref_soft/r_surf.c'
]

deps = [
    libm_dep,
    libx11_dep,
    libxext_dep,
    xxf86dga_dep
]

library(
    'ref_softx',
    sources,
    name_prefix: '',
    dependencies: deps,
    install: true
)

#
# Quake 2 engine OpenGL renderer
#

sources = [
    'game/q_shared.c',
    'linux/gl_glx.c',
    'linux/glob.c',
    'linux/q_shlinux.c',
    'linux/qgl_linux.c',
    'ref_gl/gl_draw.c',
    'ref_gl/gl_image.c',
    'ref_gl/gl_light.c',
    'ref_gl/gl_mesh.c',
    'ref_gl/gl_model.c',
    'ref_gl/gl_rmain.c',
    'ref_gl/gl_rmisc.c',
    'ref_gl/gl_rsurf.c',
    'ref_gl/gl_warp.c'
]

deps = [
    libm_dep,
    libdl_dep,
    libx11_dep,
    libxext_dep,
    xxf86dga_dep,
    xxf86vm_dep
]

library(
    'ref_glx',
    sources,
    name_prefix: '',
    dependencies: deps,
    install: true
)
