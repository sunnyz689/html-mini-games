# html-mini-games

零依赖的单文件 HTML 小游戏合集。不需要 npm、不需要构建，打开即玩。

## 游戏列表

| 游戏 | 入口 | 外部依赖 | 离线可玩 |
|---|---|---|---|
| 末日房车 · AI 求生记 | [`rv/apocalypse-rv-game.html`](rv/apocalypse-rv-game.html) | 无 | ✅ |
| 末日房车逃亡（网格版） | [`rv/房车demo-spark.html`](rv/房车demo-spark.html) | 无 | ✅ |
| 第一人称 3D 飞行 | [`flight-3d.html`](flight-3d.html) | Three.js r128（cdnjs） | ⚠ 需联网 |

## 玩法

### 末日房车 · AI 求生记
方向键 / WASD 移动房车，`空格` 冲撞加速，`1`–`3` 切换武器，`E` 进入检查站。在末日公路上尽可能久地生存下去。

### 末日房车逃亡（网格版）
同一个题材的另一版实现：网格地图 + 车辆状态（燃油/耐久度/士气/载重）+ 成员状态（驾驶员/机械师/医生）+ 物资库存 + NPC 对话。更偏"生存管理"而非动作。

### 第一人称 3D 飞行
W/A/S/D 控制方向，`空格` 加速，穿过检查点得分，避开岩石与地面。

## 运行方式

```bash
# 直接双击 html 文件即可（末日房车两个版本完全离线可玩）
# 或者起一个本地静态服务器
python -m http.server 8000
# 访问 http://localhost:8000/rv/apocalypse-rv-game.html
```

## 关于 CDN

`flight-3d.html` 从 cdnjs 拉取 Three.js r128。如果你的网络访问 cdnjs 不稳定，把 `three.min.js` 下载到本地、改写那一行 `<script src>` 即可。其余两个游戏完全不依赖网络。

## License

MIT
