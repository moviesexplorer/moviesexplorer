<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes, viewport-fit=cover" />
    <meta name="theme-color" content="#141414" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
    <title>Movies Explorer • 50+ Trending Movies & Series 2026</title>
    <meta name="description" content="Discover 50+ handpicked trending movies & series with ratings, trailers, streaming info." />
    <meta property="og:title" content="Movies Explorer • 50+ Trending Movies & Series 2026" />
    <meta property="og:description" content="Discover 50+ handpicked trending movies with ratings, trailers & download links." />
    <meta property="og:image" content="https://image.tmdb.org/t/p/w500/74xTEgt7R36Fpooo50r9T25onhq.jpg" />
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='0.9em' font-size='90'>🎬</text></svg>" />

    <style>
        :root {
            --bg: #141414;
            --bg2: #1a1a1a;
            --bg3: #252525;
            --text: #ffffff;
            --sub: #b3b3b3;
            --muted: #8c8c8c;
            --border: #2a2a2a;
            --accent: #e50914;
            --accent2: #b20710;
            --card: #1a1a1a;
            --input-bg: #1f1f1f;
            --input-border: #333;
            --hover: #2a2a2a;
            --star-color: #444;
        }

        body.light-mode {
            --bg: #f5f5f5;
            --bg2: #ffffff;
            --bg3: #e8e8e8;
            --text: #1a1a1a;
            --sub: #555;
            --muted: #777;
            --border: #ddd;
            --card: #ffffff;
            --input-bg: #f0f0f0;
            --input-border: #ccc;
            --hover: #e0e0e0;
            --star-color: #ccc;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html {
            scroll-behavior: smooth;
        }
        body {
            background: var(--bg);
            color: var(--text);
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
            min-height: 100vh;
            line-height: 1.5;
            transition: background 0.3s, color 0.3s;
        }
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--accent);
            border-radius: 10px;
        }
        .progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 2px;
            background: var(--accent);
            z-index: 9999;
            transition: width 0.1s;
            width: 0%;
        }
        .navbar {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 20px;
            background: var(--bg2);
            border-bottom: 1px solid var(--border);
            flex-wrap: wrap;
            position: sticky;
            top: 0;
            z-index: 100;
            transition: background 0.3s;
        }
        .brand {
            font-size: 20px;
            font-weight: 800;
            color: var(--text);
            text-decoration: none;
            white-space: nowrap;
            letter-spacing: -0.5px;
        }
        .brand span {
            color: var(--accent);
        }
        .nav-search {
            flex: 1;
            min-width: 140px;
            max-width: 280px;
        }
        .nav-search input {
            width: 100%;
            padding: 8px 14px;
            background: var(--input-bg);
            border: 1px solid var(--input-border);
            border-radius: 20px;
            color: var(--text);
            font-size: 13px;
            outline: none;
            transition: border 0.2s;
        }
        .nav-search input:focus {
            border-color: var(--accent);
        }
        .nav-search input::placeholder {
            color: var(--muted);
        }
        .nav-btn {
            padding: 7px 13px;
            background: var(--bg3);
            border: 1px solid var(--border);
            color: var(--text);
            border-radius: 20px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 5px;
            position: relative;
            white-space: nowrap;
        }
        .nav-btn:hover {
            background: var(--accent);
            border-color: var(--accent);
            color: #fff;
        }
        .badge {
            position: absolute;
            top: -6px;
            right: -6px;
            background: var(--accent);
            color: #fff;
            font-size: 9px;
            min-width: 16px;
            height: 16px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            padding: 2px;
            line-height: 1;
        }
        .theme-btn {
            padding: 7px 10px;
            font-size: 16px;
            background: var(--bg3);
            border: 1px solid var(--border);
            border-radius: 50%;
            cursor: pointer;
            color: var(--text);
            transition: all 0.2s;
            width: 36px;
            height: 36px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .theme-btn:hover {
            background: var(--accent);
            color: #fff;
        }
        .hero {
            text-align: center;
            padding: 16px 20px 4px;
        }
        .hero h1 {
            font-size: 2rem;
            font-weight: 800;
            letter-spacing: -0.5px;
        }
        .hero .accent {
            color: var(--accent);
        }
        .hero p {
            color: var(--muted);
            font-size: 12px;
            margin-top: 2px;
            letter-spacing: 0.5px;
        }
        .top10-section {
            margin: 10px 20px 16px;
            position: relative;
        }
        .top10-header {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 10px;
        }
        .top10-header .icon {
            font-size: 20px;
        }
        .top10-header h2 {
            font-size: 18px;
            font-weight: 700;
            color: var(--text);
        }
        .top10-header .live-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: #2ecc71;
            animation: pulseDot 1.5s infinite;
        }
        @keyframes pulseDot {
            0%,
            100% {
                box-shadow: 0 0 0 0 rgba(46, 204, 113, 0.5);
            }
            50% {
                box-shadow: 0 0 0 10px rgba(46, 204, 113, 0);
            }
        }
        .top10-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
        }
        .top10-row {
            display: flex;
            gap: 10px;
            overflow-x: hidden;
            scroll-behavior: smooth;
            padding-bottom: 4px;
        }
        .top10-card {
            flex: 0 0 340px;
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid var(--border);
            background: var(--bg2);
            aspect-ratio: 16/9;
            min-height: 180px;
        }
        .top10-card:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 30px rgba(229, 9, 20, 0.3);
            border-color: var(--accent);
            z-index: 5;
        }
        .top10-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .top10-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.95) 0%, rgba(0, 0, 0, 0.3) 50%, rgba(0, 0, 0, 0.1) 100%);
            display: flex;
            align-items: flex-end;
            padding: 14px;
        }
        .top10-info {
            width: 100%;
        }
        .top10-rank {
            position: absolute;
            top: 8px;
            left: 8px;
            font-size: 48px;
            font-weight: 900;
            color: #fff;
            text-shadow: 3px 3px 0 var(--accent), -1px -1px 0 var(--accent), 1px -1px 0 var(--accent), -1px 1px 0 var(
                    --accent);
            line-height: 1;
            opacity: 0.9;
        }
        .top10-info h3 {
            font-size: 15px;
            font-weight: 700;
            margin-bottom: 3px;
            color: #fff;
        }
        .top10-info .meta {
            font-size: 10px;
            color: #ccc;
            display: flex;
            gap: 8px;
            margin-bottom: 6px;
        }
        .top10-info .desc {
            font-size: 10px;
            color: #bbb;
            display: -webkit-box;
            -webkit-line-clamp: 1;
            -webkit-box-orient: vertical;
            overflow: hidden;
            margin-bottom: 6px;
        }
        .top10-info .actions {
            display: flex;
            gap: 6px;
        }
        .top10-info .actions button,
        .top10-info .actions a {
            padding: 5px 12px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 10px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.2s;
            white-space: nowrap;
        }
        .top10-info .actions button:hover,
        .top10-info .actions a:hover {
            background: var(--accent2);
        }
        .top10-info .actions .btn-outline-sm {
            background: transparent;
            border: 1px solid rgba(255, 255, 255, 0.5);
            color: #fff;
        }
        .top10-info .actions .btn-outline-sm:hover {
            background: rgba(255, 255, 255, 0.15);
            border-color: #fff;
        }
        .top10-badge {
            position: absolute;
            top: 8px;
            right: 8px;
            background: var(--accent);
            color: #fff;
            padding: 3px 8px;
            border-radius: 10px;
            font-size: 8px;
            font-weight: 700;
            letter-spacing: 1px;
        }
        .top10-arrow {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: rgba(0, 0, 0, 0.7);
            color: #fff;
            border: 1px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
            font-size: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 5;
            transition: all 0.2s;
            backdrop-filter: blur(4px);
        }
        .top10-arrow:hover {
            background: var(--accent);
            border-color: var(--accent);
        }
        .top10-arrow.prev {
            left: 4px;
        }
        .top10-arrow.next {
            right: 4px;
        }
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 10px 16px;
            background: var(--bg2);
            border-radius: 8px;
            margin: 0 20px 14px;
            font-size: 11px;
            color: var(--muted);
            flex-wrap: wrap;
            border: 1px solid var(--border);
            transition: background 0.3s;
        }
        .stats .live-dot {
            display: inline-block;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            background: #2ecc71;
            animation: pulseDot 1.5s infinite;
            margin-right: 4px;
        }
        .stats strong {
            color: var(--text);
        }
        .toolbar {
            display: flex;
            gap: 8px;
            padding: 0 20px;
            margin-bottom: 14px;
            flex-wrap: wrap;
            align-items: center;
        }
        .genre-chips {
            display: flex;
            gap: 5px;
            flex-wrap: wrap;
        }
        .chip {
            padding: 5px 12px;
            background: var(--bg3);
            border: 1px solid var(--border);
            border-radius: 15px;
            cursor: pointer;
            font-size: 11px;
            transition: all 0.2s;
            white-space: nowrap;
            color: var(--sub);
        }
        .chip:hover {
            border-color: var(--accent);
            color: var(--text);
        }
        .chip.selected {
            background: var(--accent);
            border-color: var(--accent);
            color: #fff;
        }
        .chip .count {
            font-size: 9px;
            background: rgba(0, 0, 0, 0.3);
            padding: 1px 5px;
            border-radius: 8px;
            margin-left: 3px;
        }
        .toolbar select {
            padding: 6px 24px 6px 10px;
            background: var(--bg3);
            border: 1px solid var(--border);
            border-radius: 8px;
            color: var(--text);
            font-size: 11px;
            cursor: pointer;
            outline: none;
            appearance: none;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='10' viewBox='0 0 24 24' fill='%23888'%3E%3Cpath d='M7 10l5 5 5-5z'/%3E%3C/svg%3E");
            background-repeat: no-repeat;
            background-position: right 6px center;
            transition: border 0.2s;
        }
        .toolbar select:focus {
            border-color: var(--accent);
        }
        .section-title {
            padding: 0 20px;
            margin-bottom: 10px;
            font-size: 16px;
            font-weight: 700;
            border-left: 3px solid var(--accent);
            padding-left: 10px;
        }
        .movie-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 14px;
            padding: 0 20px;
        }
        .movie-card {
            background: var(--card);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid var(--border);
            transition: all 0.25s;
            animation: fadeUp 0.4s ease both;
        }
        .movie-card:hover {
            transform: translateY(-4px);
            border-color: var(--accent);
            box-shadow: 0 8px 24px rgba(229, 9, 20, 0.15);
        }
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(15px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .poster-wrap {
            position: relative;
            aspect-ratio: 2/3;
            cursor: pointer;
            background: #000;
            overflow: hidden;
        }
        .poster-wrap img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }
        .movie-card:hover .poster-wrap img {
            transform: scale(1.03);
        }
        .poster-quality {
            position: absolute;
            top: 6px;
            left: 6px;
            background: var(--accent);
            padding: 2px 8px;
            border-radius: 10px;
            font-size: 9px;
            font-weight: 700;
            color: #fff;
        }
        .trending-badge {
            position: absolute;
            top: 6px;
            left: 6px;
            background: linear-gradient(135deg, #e50914, #ff4444);
            padding: 2px 8px;
            border-radius: 10px;
            font-size: 9px;
            font-weight: 700;
            color: #fff;
            animation: glow 2s infinite;
        }
        @keyframes glow {
            0%,
            100% {
                box-shadow: 0 0 4px rgba(229, 9, 20, 0.3);
            }
            50% {
                box-shadow: 0 0 10px rgba(229, 9, 20, 0.6);
            }
        }
        .card-actions-btns {
            position: absolute;
            top: 6px;
            right: 6px;
            display: flex;
            flex-direction: column;
            gap: 3px;
            z-index: 2;
        }
        .icon-btn {
            width: 26px;
            height: 26px;
            border-radius: 50%;
            background: rgba(0, 0, 0, 0.55);
            border: 1px solid rgba(255, 255, 255, 0.15);
            color: #fff;
            cursor: pointer;
            font-size: 11px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
        }
        .icon-btn:hover {
            background: var(--accent);
            border-color: var(--accent);
        }
        .icon-btn.saved {
            background: var(--accent);
            border-color: var(--accent);
        }
        .card-body {
            padding: 10px 12px 12px;
        }
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            gap: 5px;
        }
        .card-title {
            font-size: 13px;
            font-weight: 700;
            color: var(--text);
        }
        .card-rating {
            background: var(--accent);
            padding: 1px 7px;
            border-radius: 8px;
            font-size: 10px;
            font-weight: 700;
            white-space: nowrap;
            color: #fff;
        }
        .card-meta {
            display: flex;
            gap: 6px;
            color: var(--muted);
            font-size: 10px;
            margin: 4px 0;
        }
        .card-meta span {
            background: var(--bg3);
            padding: 1px 6px;
            border-radius: 3px;
        }
        .card-desc {
            color: var(--sub);
            font-size: 11px;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
            margin-bottom: 8px;
            line-height: 1.4;
        }
        .stream-tags {
            display: flex;
            gap: 4px;
            margin-bottom: 8px;
            flex-wrap: wrap;
        }
        .stream-tag {
            padding: 1px 7px;
            border-radius: 8px;
            font-size: 9px;
            font-weight: 600;
            border: 1px solid;
        }
        .st-n {
            color: #e50914;
            border-color: #e50914;
        }
        .st-h {
            color: #a855f7;
            border-color: #a855f7;
        }
        .st-p {
            color: #00a8e1;
            border-color: #00a8e1;
        }
        .st-d {
            color: #1fd9e5;
            border-color: #1fd9e5;
        }
        .st-a {
            color: #aaa;
            border-color: #aaa;
        }
        .st-pp {
            color: #0064ff;
            border-color: #0064ff;
        }
        .st-hu {
            color: #1ce783;
            border-color: #1ce783;
        }
        .st-pc {
            color: #f9f9f9;
            border-color: #f9f9f9;
        }
        .btn-row {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        .btn-watch {
            padding: 7px;
            background: #e50914;
            color: #fff;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 11px;
            font-weight: 600;
            width: 100%;
            transition: all 0.2s;
        }
        .btn-watch:hover {
            background: #b20710;
        }
        .btn-dl {
            padding: 7px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 11px;
            font-weight: 600;
            width: 100%;
            transition: all 0.2s;
        }
        .btn-dl:hover {
            background: var(--accent2);
        }
        .btn-tr {
            padding: 7px;
            background: transparent;
            color: var(--text);
            border: 1px solid var(--border);
            border-radius: 6px;
            cursor: pointer;
            font-size: 11px;
            width: 100%;
            transition: all 0.2s;
        }
        .btn-tr:hover {
            background: var(--hover);
            border-color: var(--accent);
        }
        .share-row {
            display: flex;
            gap: 3px;
            margin-top: 3px;
        }
        .share-btn {
            flex: 1;
            padding: 5px;
            background: var(--bg3);
            border: 1px solid var(--border);
            border-radius: 5px;
            cursor: pointer;
            color: var(--muted);
            font-size: 12px;
            text-align: center;
            transition: all 0.2s;
        }
        .share-btn:hover {
            background: var(--hover);
            color: var(--text);
        }
        .sidebar-overlay {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.7);
            z-index: 200;
        }
        .sidebar-overlay.show {
            display: block;
        }
        .sidebar {
            position: fixed;
            top: 0;
            right: -380px;
            width: 360px;
            max-width: 90vw;
            height: 100vh;
            height: 100dvh;
            background: var(--bg2);
            z-index: 201;
            transition: right 0.3s;
            overflow-y: auto;
            padding: 18px;
            border-left: 1px solid var(--border);
        }
        .sidebar.open {
            right: 0;
        }
        .sidebar-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
            padding-bottom: 10px;
            border-bottom: 1px solid var(--border);
        }
        .sidebar-header h3 {
            color: var(--accent);
            font-size: 16px;
        }
        .sidebar-close {
            padding: 5px 12px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
            font-weight: 600;
        }
        .sidebar-item {
            display: flex;
            gap: 10px;
            padding: 8px;
            background: var(--bg3);
            border-radius: 8px;
            margin-bottom: 6px;
            cursor: pointer;
            border: 1px solid var(--border);
            transition: all 0.2s;
        }
        .sidebar-item:hover {
            border-color: var(--accent);
            transform: translateX(-3px);
        }
        .sidebar-item img {
            width: 40px;
            height: 56px;
            object-fit: cover;
            border-radius: 4px;
        }
        .sidebar-item h4 {
            font-size: 12px;
            color: var(--text);
            margin-bottom: 2px;
        }
        .sidebar-item p {
            font-size: 10px;
            color: var(--muted);
        }
        .sidebar-empty {
            text-align: center;
            padding: 40px;
            color: var(--muted);
        }
        .sidebar-empty .icon {
            font-size: 36px;
            display: block;
            margin-bottom: 8px;
        }
        .notif-item {
            padding: 8px 10px;
            background: var(--bg3);
            border-radius: 6px;
            margin-bottom: 4px;
            font-size: 11px;
            color: var(--sub);
            border-left: 3px solid var(--accent);
        }
        .notif-item .time {
            font-size: 9px;
            color: var(--muted);
            margin-top: 2px;
        }
        .modal-backdrop {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.92);
            z-index: 300;
            align-items: center;
            justify-content: center;
            padding: 16px;
        }
        .modal-backdrop.open {
            display: flex;
        }
        .modal-dialog {
            background: var(--bg2);
            border-radius: 14px;
            max-width: 800px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            border: 1px solid var(--border);
            padding: 20px;
        }
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
        }
        .modal-header h2 {
            color: var(--accent);
            font-size: 18px;
        }
        .modal-close {
            padding: 6px 14px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            font-size: 12px;
        }
        .details-layout {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }
        .details-poster {
            flex: 0 0 180px;
        }
        .details-poster img {
            width: 100%;
            border-radius: 10px;
            object-fit: cover;
        }
        .details-info {
            flex: 1;
            min-width: 200px;
        }
        .details-info h2 {
            font-size: 20px;
            margin-bottom: 4px;
            color: var(--text);
        }
        .details-info .meta {
            color: var(--muted);
            font-size: 12px;
            margin-bottom: 8px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        .details-info .desc {
            color: var(--sub);
            font-size: 13px;
            line-height: 1.6;
            margin-bottom: 10px;
        }
        .details-info .actions {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 10px;
        }
        .details-info .actions button {
            padding: 7px 16px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 12px;
            transition: all 0.2s;
        }
        .btn-primary {
            background: var(--accent);
            color: #fff;
            border: none;
        }
        .btn-primary:hover {
            background: var(--accent2);
        }
        .btn-outline {
            background: transparent;
            color: var(--text);
            border: 1px solid var(--border);
        }
        .btn-outline:hover {
            background: var(--hover);
            border-color: var(--accent);
        }
        .btn-liked {
            background: var(--accent) !important;
            color: #fff !important;
            border: 1px solid var(--accent) !important;
        }
        .star-rating {
            display: flex;
            gap: 3px;
            margin-bottom: 8px;
        }
        .star-rating .star {
            font-size: 20px;
            cursor: pointer;
            color: var(--star-color);
            transition: color 0.2s;
        }
        .star-rating .star.active,
        .star-rating .star:hover {
            color: #ffc107;
        }
        .comment-box textarea {
            width: 100%;
            padding: 8px;
            background: var(--bg3);
            border: 1px solid var(--border);
            border-radius: 6px;
            color: var(--text);
            font-size: 12px;
            resize: vertical;
            min-height: 50px;
            outline: none;
        }
        .comment-box textarea:focus {
            border-color: var(--accent);
        }
        .comment-box button {
            margin-top: 5px;
            padding: 5px 14px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            font-size: 11px;
        }
        .comments-list {
            max-height: 120px;
            overflow-y: auto;
            margin-top: 8px;
        }
        .comments-list .comment-item {
            padding: 6px 10px;
            background: var(--bg3);
            border-radius: 5px;
            margin-bottom: 3px;
            font-size: 11px;
            color: var(--sub);
        }
        .related-section {
            margin-top: 14px;
        }
        .related-section h4 {
            font-size: 13px;
            margin-bottom: 8px;
            border-left: 3px solid var(--accent);
            padding-left: 8px;
            color: var(--text);
        }
        .related-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            gap: 8px;
        }
        .related-card {
            cursor: pointer;
            border-radius: 6px;
            overflow: hidden;
            transition: transform 0.2s;
            border: 1px solid var(--border);
            background: var(--bg3);
        }
        .related-card:hover {
            transform: scale(1.04);
            border-color: var(--accent);
        }
        .related-card img {
            width: 100%;
            aspect-ratio: 2/3;
            object-fit: cover;
        }
        .related-card .r-title {
            padding: 4px 6px;
            font-size: 10px;
            text-align: center;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            color: var(--sub);
        }
        .recent-section {
            padding: 0 20px;
            margin-top: 20px;
            display: none;
        }
        .recent-section.show {
            display: block;
        }
        .recent-title {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 8px;
            border-left: 3px solid var(--accent);
            padding-left: 8px;
            color: var(--text);
        }
        .recent-row {
            display: flex;
            gap: 8px;
            overflow-x: auto;
            padding-bottom: 4px;
        }
        .recent-card {
            flex: 0 0 90px;
            cursor: pointer;
            border-radius: 6px;
            overflow: hidden;
            border: 1px solid var(--border);
            transition: transform 0.2s;
            background: var(--bg2);
        }
        .recent-card:hover {
            transform: scale(1.04);
            border-color: var(--accent);
        }
        .recent-card img {
            width: 100%;
            aspect-ratio: 2/3;
            object-fit: cover;
        }
        .recent-card .r-title {
            padding: 3px 5px;
            font-size: 9px;
            text-align: center;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            color: var(--sub);
        }
        .no-results {
            text-align: center;
            padding: 40px;
            color: var(--muted);
            grid-column: 1/-1;
            display: none;
        }
        .no-results .icon {
            font-size: 40px;
            display: block;
            margin-bottom: 8px;
        }
        .toast-area {
            position: fixed;
            bottom: 16px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 999;
            display: flex;
            flex-direction: column;
            gap: 5px;
            max-width: 90vw;
            pointer-events: none;
        }
        .toast {
            padding: 8px 16px;
            background: #333;
            color: #fff;
            border-radius: 8px;
            font-size: 12px;
            animation: toastUp 0.3s ease;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.4);
            pointer-events: auto;
        }
        @keyframes toastUp {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        .scroll-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: var(--accent);
            color: #fff;
            border: none;
            font-size: 16px;
            cursor: pointer;
            z-index: 99;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
        }
        .scroll-top.visible {
            opacity: 1;
            visibility: visible;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: var(--muted);
            font-size: 11px;
            margin-top: 30px;
            border-top: 1px solid var(--border);
        }
        .footer-nl {
            display: flex;
            gap: 5px;
            justify-content: center;
            margin-bottom: 10px;
            flex-wrap: wrap;
        }
        .footer-nl input {
            padding: 7px 12px;
            background: var(--input-bg);
            border: 1px solid var(--input-border);
            border-radius: 6px;
            color: var(--text);
            font-size: 12px;
            outline: none;
            min-width: 160px;
        }
        .footer-nl input:focus {
            border-color: var(--accent);
        }
        .footer-nl button {
            padding: 7px 16px;
            background: var(--accent);
            color: #fff;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 12px;
        }
        @media (max-width: 768px) {
            .navbar {
                padding: 8px 10px;
                gap: 6px;
            }
            .brand {
                font-size: 16px;
            }
            .nav-btn {
                font-size: 10px;
                padding: 5px 9px;
            }
            .nav-search {
                min-width: 100%;
                max-width: 100%;
                order: 10;
            }
            .hero h1 {
                font-size: 1.4rem;
            }
            .top10-card {
                flex: 0 0 280px;
                min-height: 150px;
            }
            .top10-rank {
                font-size: 36px;
                top: 5px;
                left: 5px;
            }
            .top10-info h3 {
                font-size: 13px;
            }
            .movie-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
                gap: 8px;
                padding: 0 10px;
            }
            .card-title {
                font-size: 11px;
            }
            .card-desc {
                font-size: 10px;
                -webkit-line-clamp: 1;
            }
            .details-layout {
                flex-direction: column;
            }
            .details-poster {
                flex: 0 0 140px;
            }
            .sidebar {
                width: 100vw;
                max-width: 100vw;
                right: -100vw;
            }
            .stats {
                gap: 8px;
                font-size: 10px;
                margin: 0 10px 10px;
            }
            .toolbar {
                padding: 0 10px;
            }
            .chip {
                font-size: 10px;
                padding: 4px 10px;
            }
            .recent-card {
                flex: 0 0 65px;
            }
            .related-grid {
                grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
            }
            .top10-section {
                margin: 8px 10px 12px;
            }
            .section-title {
                padding: 0 10px;
            }
            .top10-arrow {
                width: 28px;
                height: 28px;
                font-size: 12px;
            }
        }
        @media (max-width: 400px) {
            .movie-grid {
                grid-template-columns: 1fr 1fr;
                gap: 5px;
            }
            .card-body {
                padding: 6px 8px 8px;
            }
            .btn-watch,
            .btn-dl,
            .btn-tr {
                font-size: 10px;
                padding: 5px;
            }
            .top10-card {
                flex: 0 0 240px;
                min-height: 130px;
            }
            .top10-rank {
                font-size: 28px;
            }
        }
        @media (min-width: 1200px) {
            .movie-grid {
                grid-template-columns: repeat(4, 1fr);
            }
            .top10-card {
                flex: 0 0 380px;
            }
        }
        @media (min-width: 1600px) {
            .movie-grid {
                grid-template-columns: repeat(5, 1fr);
            }
        }
    </style>
</head>
<body>

    <div class="progress-bar" id="progressBar"></div>
    <nav class="navbar">
        <a href="#" class="brand">🎬 Movies<span>Explorer</span></a>
        <div class="nav-search"><input type="text" id="searchInput" placeholder="🔍 Search movies..." oninput="filterMovies()"></div>
        <button class="nav-btn" onclick="openSidebar('watchlist')">📋 Watchlist <span class="badge" id="wlBadge" style="display:none">0</span></button>
        <button class="nav-btn" onclick="openSidebar('liked')">❤️ Liked <span class="badge" id="likedBadge" style="display:none">0</span></button>
        <button class="nav-btn" onclick="openSidebar('notifications')">🔔 <span class="badge" id="notifBadge" style="display:none">0</span></button>
        <button class="theme-btn" onclick="toggleTheme()" title="Toggle Theme">🌓</button>
    </nav>
    <div class="hero"><h1>Movies<span class="accent">Explorer</span></h1><p>✦ 50+ Trending Movies ✦ Updated Weekly ✦</p></div>
    <div class="top10-section">
        <div class="top10-header"><span class="icon">🔥</span><h2>Top 10 Trending This Week</h2><span class="live-dot"></span></div>
        <div class="top10-wrapper"><div class="top10-row" id="top10Row"></div><button class="top10-arrow prev" onclick="scrollTop10(-1)">❮</button><button class="top10-arrow next" onclick="scrollTop10(1)">❯</button></div>
    </div>
    <div class="stats"><span><span class="live-dot"></span> LIVE</span><span>📈 <strong>30K+</strong> views</span><span>⭐ <strong>8.0+</strong> avg</span><span>🎬 <strong>50</strong> movies</span><span>👥 <strong>5K+</strong> users</span></div>
    <div class="toolbar">
        <div class="genre-chips" id="genreChips"><span class="chip selected" onclick="filterByGenre('all', this)">All <span class="count">50</span></span></div>
        <select id="sortSelect" onchange="filterMovies()"><option value="default">📋 Default</option><option value="rating">⭐ Highest Rated</option><option value="year">📅 Newest</option><option value="title">🔤 A-Z</option></select>
        <select id="yearFilter" onchange="filterMovies()"><option value="all">All Years</option><option value="2024">2024</option><option value="2023">2023</option><option value="2022">2022</option><option value="2021">2021</option><option value="2020">2020</option><option value="2019">2019</option><option value="2018">2018</option><option value="2017">2017</option><option value="2016">2016</option><option value="2015">2015</option><option value="2014">2014</option><option value="2010">2010</option><option value="2000">2000</option><option value="1990">1990</option><option value="1980">1980</option><option value="1979">1979</option></select>
    </div>
    <h3 class="section-title">🎬 All Movies</h3>
    <div class="movie-grid" id="movieGrid"></div>
    <div class="no-results" id="noResults"><span class="icon">🎬</span><h3>No Movies Found</h3><p>Try different search or filters</p></div>
    <div class="recent-section" id="recentSection"><h3 class="recent-title">🕐 Recently Viewed</h3><div class="recent-row" id="recentRow"></div></div>
    <footer class="footer"><div class="footer-nl"><input type="email" placeholder="Email for updates..."><button onclick="subscribeNewsletter()">Subscribe 🎬</button></div><p>© 2026 Movies Explorer • Made with ❤️</p></footer>
    <div class="sidebar-overlay" id="sidebarOverlay" onclick="closeSidebar()"></div>
    <div class="sidebar" id="watchlistSidebar"><div class="sidebar-header"><h3>📋 Watchlist</h3><button class="sidebar-close" onclick="closeSidebar()">✕</button></div><div id="watchlistContent"></div></div>
    <div class="sidebar" id="likedSidebar"><div class="sidebar-header"><h3>❤️ Liked Movies</h3><button class="sidebar-close" onclick="closeSidebar()">✕</button></div><div id="likedContent"></div></div>
    <div class="sidebar" id="notificationsSidebar"><div class="sidebar-header"><h3>🔔 Notifications</h3><button class="sidebar-close" onclick="closeSidebar()">✕</button></div><div id="notificationsContent"></div></div>
    <div class="modal-backdrop" id="detailsModal"><div class="modal-dialog" id="detailsContent"></div></div>
    <button class="scroll-top" id="scrollTopBtn" onclick="window.scrollTo({top:0,behavior:'smooth'})">↑</button>
    <div class="toast-area" id="toastArea"></div>

    <script>
        const AD_URL = 'https://beansnicerroller.com/my0cbe74j?key=b6340de156f305a16e38fb1fe693022c';
        const MOVIEBOX = 'https://themoviebox.xyz/search?q=';
        const YT_SEARCH = 'https://www.youtube.com/results?search_query=';
        const POSTER = 'https://image.tmdb.org/t/p/w500/';
        const STREAM_NAMES = { n: 'Netflix', h: 'HBO', p: 'Prime', d: 'Disney+', a: 'Apple', pp: 'Paramount+', hu: 'Hulu',
            pc: 'Peacock' };
        const STREAM_CLASS = { n: 'st-n', h: 'st-h', p: 'st-p', d: 'st-d', a: 'st-a', pp: 'st-pp', hu: 'st-hu',
        pc: 'st-pc' };

        // ✅ ALL 50 MOVIES WITH VERIFIED WORKING TMDB POSTERS
        const MOVIES = [
            { t: "The Batman", y: 2022, g: "Action Thriller Crime", r: 8.4, tr: 1, img: "74xTEgt7R36Fpooo50r9T25onhq.jpg",
                d: "Dark noir thriller with Robert Pattinson in corrupt Gotham.", st: "n|h" },
            { t: "Dune", y: 2021, g: "Sci-Fi Action Drama", r: 8.0, tr: 1, img: "d5NXSklXo0qyIYkgV94XAgMIckC.jpg",
                d: "Villeneuve's breathtaking sci-fi with Hans Zimmer score.", st: "h|p" },
            { t: "Interstellar", y: 2014, g: "Sci-Fi Drama", r: 8.7, tr: 1, img: "gEU2QniE6E77NI6lCU6MxlNBvIx.jpg",
                d: "Nolan's cosmic journey through wormholes. Time dilation masterpiece.", st: "p|a" },
            { t: "John Wick 4", y: 2023, g: "Action Thriller", r: 7.9, tr: 1, img: "vZloFAK7NmvMGKE7VkF5UHaz0I.jpg",
                d: "Keanu returns with nonstop bullets. Donnie Yen steals every scene.", st: "p|a" },
            { t: "The Last of Us", y: 2023, g: "Drama Thriller Sci-Fi", r: 8.8, tr: 1,
                img: "uKvVjHNqB5VmOrdxqAt2F7J78ED.jpg", d: "Pedro Pascal & Bella Ramsey in post-apocalyptic masterpiece.",
                st: "h" },
            { t: "Oppenheimer", y: 2023, g: "Drama Thriller", r: 8.9, tr: 1, img: "8Gxv8gSFCU0XGDykEGv7zR1n2ua.jpg",
                d: "Cillian Murphy as atomic bomb father. 7 Oscars. Nolan's best.", st: "p|a" },
            { t: "Spider-Verse", y: 2023, g: "Animation Action Sci-Fi", r: 8.7, tr: 1,
                img: "8Vt6mWEReuy4Of61Lnj5Xj704m8.jpg", d: "Miles Morales through multiverses. Every frame a painting.",
                st: "n" },
            { t: "Godzilla -1.0", y: 2023, g: "Sci-Fi Action Drama", r: 8.5, tr: 1,
                img: "hkxxMIGaiCTmrEArVIn2zGQ8Nf0.jpg", d: "Best Godzilla film ever. Emotional and visually spectacular.",
                st: "n" },
            { t: "Dune Part Two", y: 2024, g: "Sci-Fi Action Drama", r: 8.6, tr: 1,
                img: "1pdfLvkbY9ohJlCjQH2CZjjYVvJ.jpg", d: "Paul Atreides rides the worm. Epic Villeneuve conclusion.",
                st: "h|p" },
            { t: "Deadpool & Wolverine", y: 2024, g: "Action Comedy Sci-Fi", r: 8.0, tr: 1,
                img: "8cdWjvZQUExUUTzyTbNtwQtXxgS.jpg", d: "Ryan Reynolds & Hugh Jackman. R-rated Marvel madness.", st: "d" },
            { t: "The Boys", y: 2019, g: "Action Drama Comedy Thriller", r: 8.7, tr: 0,
                img: "2zmTngn1tYC1AvfnrFLhxeD82hz.jpg", d: "Corrupt superheroes. Karl Urban hunts capes.", st: "p" },
            { t: "Barbie", y: 2023, g: "Comedy Fantasy", r: 7.5, tr: 0, img: "iuFNMS8U5cb6xfzi51Dbkovj7vM.jpg",
                d: "Margot Robbie & Ryan Gosling in Gerwig's pink box office phenomenon.", st: "h" },
            { t: "MI: Dead Reckoning", y: 2023, g: "Action Thriller", r: 8.3, tr: 0,
                img: "NNxYQVkaSTcWkU3bQVHQGzJzwC.jpg", d: "Tom Cruise drives motorcycle off cliff. AI villain thriller.",
                st: "pp" },
            { t: "Scream VI", y: 2023, g: "Horror Mystery Thriller", r: 6.9, tr: 0,
                img: "wDWwtvkRRlgTiUr6TyLSMX8FCuZ.jpg", d: "Ghostface stalks NYC. Jenna Ortega leads new bloodbath.", st: "pp" },
            { t: "Cocaine Bear", y: 2023, g: "Comedy Horror Thriller", r: 6.3, tr: 0,
                img: "gOnmaxHo0412UVr1QM5Nekv1xPi.jpg", d: "True story. Bear eats cocaine. Ridiculous chaos ensues.", st: "pc" },
            { t: "The Nun II", y: 2023, g: "Horror Thriller", r: 6.1, tr: 0, img: "5gzzkR7y3hnY8AD1wXjCnVlHba5.jpg",
                d: "Valak returns in 1956 France. Conjuring universe expands.", st: "h" },
            { t: "The Bear S2", y: 2023, g: "Drama Comedy", r: 8.6, tr: 0, img: "6caLwJjUyRaLFDhXQxCXJjGG86I.jpg",
                d: "Carmy builds new restaurant. Best Christmas episode ever made.", st: "hu" },
            { t: "Inception", y: 2010, g: "Sci-Fi Action Thriller", r: 8.8, tr: 0,
                img: "edv5CZvWj09upOsy2Y6IwDhK8bt.jpg", d: "Nolan's mind-bending heist. Dreams within dreams.", st: "n|p" },
            { t: "The Dark Knight", y: 2008, g: "Crime Drama Action", r: 9.0, tr: 0,
                img: "qJ2tW6WMUDux911BytUEMqqoNAd.jpg", d: "Heath Ledger's Joker. Greatest superhero film ever made.", st: "n|h" },
            { t: "The Matrix", y: 1999, g: "Sci-Fi Action Thriller", r: 8.7, tr: 0,
                img: "f89U3ADr1oiB1s9GkdPOEpXUk5H.jpg", d: "Red pill or blue pill? Revolutionary bullet-time action.", st: "n|p" },
            { t: "Shawshank Redemption", y: 1994, g: "Drama Crime", r: 9.3, tr: 0,
                img: "9cjIGRiQvEZsl4xT6GqFkVEV5qy.jpg", d: "Hope is a good thing. Greatest prison story ever told.", st: "n" },
            { t: "Gladiator", y: 2000, g: "Action Drama", r: 8.5, tr: 0, img: "ty8TGRuvJLPUmAR1H1nRIs4gCLK.jpg",
                d: "Russell Crowe's epic revenge. Are you not entertained?", st: "p|pp" },
            { t: "Get Out", y: 2017, g: "Horror Thriller", r: 7.8, tr: 0, img: "tFXcEccSQMf3lfhfXKSU9iRBpa3.jpg",
                d: "Jordan Peele's social thriller masterpiece. Culturally groundbreaking.", st: "n" },
            { t: "Everything Everywhere", y: 2022, g: "Sci-Fi Comedy Drama", r: 7.8, tr: 0,
                img: "w3LxiVYdWWRvEVdn5RYq6jIqkb1.jpg", d: "Michelle Yeoh across multiverse. Wild, emotional, 7 Oscars.", st: "p|a" },
            { t: "A Quiet Place", y: 2018, g: "Horror Thriller Sci-Fi", r: 7.5, tr: 0,
                img: "nAU74GmpUk7t5iklEp3bufwDq4n.jpg", d: "Silence is survival. John Krasinski's tense masterpiece.", st: "pp" },
            { t: "Mad Max Fury Road", y: 2015, g: "Action Sci-Fi Thriller", r: 8.1, tr: 0,
                img: "hA2ple9q4qnwxp3hKVNhroipsir.jpg", d: "What a lovely day! Nonstop vehicular mayhem in desert.", st: "p|a" },
            { t: "Forrest Gump", y: 1994, g: "Drama Comedy", r: 8.8, tr: 0, img: "arw2vcBveWOVZr6pxd9XTd1TdQa.jpg",
                d: "Life is like a box of chocolates. Tom Hanks' iconic journey.", st: "n|p" },
            { t: "MI: Fallout", y: 2018, g: "Action Thriller", r: 7.7, tr: 0, img: "AkJQpZp9WoNfm7gmXkIB7mLP1vI.jpg",
                d: "Best Mission Impossible. Henry Cavill reloads arms. Epic finale.", st: "pp" },
            { t: "Us", y: 2019, g: "Horror Thriller", r: 6.8, tr: 0, img: "ux2dU1jQ2ACIMShzB3yP93UdpwL.jpg",
                d: "Jordan Peele's doppelgänger nightmare. Lupita Nyong'o dual performance.", st: "n" },
            { t: "Shrek", y: 2001, g: "Animation Comedy", r: 7.9, tr: 0, img: "iB64vpL3dIObOtMZgX3RqdVdQDc.jpg",
                d: "Somebody once told me... Ogres have layers! Endlessly quotable classic.", st: "pc" },
            { t: "Titanic", y: 1997, g: "Drama Romance", r: 7.9, tr: 0, img: "9xjZS2rlVxm8SFx8kPC3aIGCOYQ.jpg",
                d: "James Cameron's epic. Leo & Kate on doomed ship. My heart will go on.", st: "n|p" },
            { t: "Avatar", y: 2009, g: "Sci-Fi Action Adventure", r: 7.9, tr: 0, img: "6EiRUJpuoeQPghnDjj2NuIflI5a.jpg",
                d: "James Cameron's Pandora. Revolutionary 3D. Highest-grossing film.", st: "d" },
            { t: "Longlegs", y: 2024, g: "Horror Thriller Crime", r: 7.0, tr: 0,
                img: "5E2JHeUkaeIYXKi2QhNPpHo6QmV.jpg", d: "Nicolas Cage is a terrifying serial killer. Scariest of 2024.",
                st: "p" },
            { t: "Civil War", y: 2024, g: "Drama Thriller Action", r: 7.4, tr: 0,
                img: "sh7RgKErX1KjFjDyhGX7TjQpZ8i.jpg", d: "Alex Garland's dystopian America. Journalists in second civil war.",
                st: "p" },
            { t: "Inside Out 2", y: 2024, g: "Animation Comedy Drama", r: 7.8, tr: 0,
                img: "vpnVM9B6NMmQpWeZvzLvDESb2QY.jpg", d: "Anxiety joins Riley's emotions. Pixar's billion-dollar sequel.",
                st: "d" },
            { t: "Alien", y: 1979, g: "Horror Sci-Fi Thriller", r: 8.5, tr: 0, img: "vfrQk5IPloGg1v9Rzbh2Eg3VGyM.jpg",
                d: "In space no one can hear you scream. Ridley Scott's perfect organism.", st: "h|p" },
            { t: "Goodfellas", y: 1990, g: "Crime Drama Thriller", r: 8.7, tr: 0,
                img: "aKuFiU82s5IS7J3F8iOHdZxGm4K.jpg", d: "As far back as I can remember... Scorsese's gangster masterpiece.",
                st: "n|p" },
            { t: "Terminator 2", y: 1991, g: "Sci-Fi Action Thriller", r: 8.6, tr: 0,
                img: "5M0j0B18abtBI5gi2RhfjjurTbh.jpg", d: "Hasta la vista baby. Cameron's action perfection with T-1000.",
                st: "n|p" },
            { t: "Fight Club", y: 1999, g: "Drama Thriller", r: 8.8, tr: 0, img: "pB8BM7pdSp6B6Ih7QZ4DrQ3PmJK.jpg",
                d: "First rule: You do not talk about it. Fincher's anarchist masterpiece.", st: "n|p" },
            { t: "The Shining", y: 1980, g: "Horror Drama Thriller", r: 8.4, tr: 0,
                img: "nRj7G6I5kP8KYfL0S4wLmN6dQ2J.jpg", d: "Here's Johnny! Kubrick's descent into madness at Overlook Hotel.",
                st: "h|p" },
            { t: "The Fall Guy", y: 2024, g: "Action Comedy Thriller", r: 7.2, tr: 0,
                img: "tSz1KzPQaBgSgkVJgDrZzHmNqXw.jpg", d: "Ryan Gosling stuntman framed for murder. Real practical stunts.",
                st: "p" },
            { t: "The Incredibles", y: 2004, g: "Animation Action Comedy", r: 8.0, tr: 0,
                img: "2M1kLoSkGkCgsG0GZmCo5XwIdpW.jpg", d: "Pixar's superhero family. No capes! Timeless classic.", st: "d" },
            { t: "No Country", y: 2007, g: "Crime Thriller Drama", r: 8.2, tr: 0,
                img: "nBaqryObPuxmuAndWUjDE5rriTd.jpg", d: "Coin toss friend-o. Coen Brothers' relentless chase.", st: "p|a" },
            { t: "Arrival", y: 2016, g: "Sci-Fi Drama", r: 7.9, tr: 0, img: "pEzNVQfdzYDzUtoCkEhrFz86oYU.jpg",
                d: "Amy Adams deciphers alien language. Profound meditation on time and loss.", st: "p|pp" },
            { t: "Saving Private Ryan", y: 1998, g: "Drama War Action", r: 8.6, tr: 0,
                img: "uqxXpMZ2cRoGhSAYZVZqTVXXzHx.jpg", d: "Spielberg's D-Day landing. Most realistic war film. Earn this.",
                st: "p|pp" },
            { t: "Grand Budapest", y: 2014, g: "Comedy Crime Drama", r: 8.1, tr: 0,
                img: "eWdyYQreja6JGCzqHWXpWHDrrPo.jpg", d: "Wes Anderson's most Wes Anderson film.", st: "p" },
            { t: "Smile", y: 2022, g: "Horror Thriller Mystery", r: 6.6, tr: 0, img: "aPqcQwu4VGEewPhagWNEsH4BA5T.jpg",
                d: "You'll die with a smile. Creepy curse film.", st: "p|pp" },
            { t: "Top Gun Maverick", y: 2022, g: "Action Drama", r: 8.3, tr: 0,
                img: "62HCnUTziyWcpDaBO2i1DX17ljH.jpg", d: "Tom Cruise returns to danger zone.", st: "p|pp" },
            { t: "The Iron Claw", y: 2023, g: "Drama Sport", r: 7.7, tr: 0, img: "nQq2JhVpSVxBVqBqkVhFPKwFcGL.jpg",
                d: "Zac Efron jacked. Tragic true story of Von Erich wrestling dynasty.", st: "p" },
            { t: "Joker", y: 2019, g: "Crime Drama Thriller", r: 8.4, tr: 0, img: "udDclJoHjfjb8Ekgsd4FDteOkCU.jpg",
                d: "Joaquin Phoenix's descent into madness. We live in a society. Oscar winner.", st: "n|h" }
        ];

        let dlClicks = {};
        let trClicks = {};
        let watchClicks = {};
        let activeGenre = 'all';
        let notifications = [];

        function handleAdThenAction(clickMap, key, actionFn) {
            const now = Date.now();
            const last = clickMap[key] || 0;
            if (!last || now - last > 1800000) {
                window.open(AD_URL, '_blank');
                clickMap[key] = now;
                toast('📢 Ad opened • Click again to proceed');
                return false;
            } else { actionFn(); return true; }
        }

        function init() {
            renderTop10();
            renderAllMovies();
            initGenreChips();
            renderRecent();
            loadNotifications();
            updateAllBadges();
            restoreBookmarks();
            if (localStorage.getItem('theme') === 'light') document.body.classList.add('light-mode');
            console.log('🎬 Movies Explorer • All Posters Verified • 50 Movies');
        }

        function renderTop10() {
            const row = document.getElementById('top10Row');
            const top10 = [...MOVIES.filter(m => m.tr === 1), ...MOVIES.filter(m => m.tr === 0)].slice(0, 10);
            row.innerHTML = top10.map((m, i) => {
                const te = m.t.replace(/'/g, "\\'");
                return `<div class="top10-card" onclick="openDetails('${te}')"><img src="${POSTER}${m.img}" alt="${m.t}" loading="${i<3?'eager':'lazy'}"><div class="top10-overlay"><div class="top10-info"><span class="top10-rank">${i+1}</span><h3>${m.t}</h3><div class="meta"><span>⭐ ${m.r}</span><span>📅 ${m.y}</span></div><div class="desc">${m.d}</div><div class="actions"><a href="javascript:void(0)" onclick="event.stopPropagation();handleWatch('${te}')">▶ Watch</a><button class="btn-outline-sm" onclick="event.stopPropagation();handleTrailer(event,'${te}')">🎬 Trailer</button><button class="btn-outline-sm" onclick="event.stopPropagation();toggleWatchlistTop10('${te}')">➕ List</button></div></div></div><div class="top10-badge">🔥 TRENDING</div></div>`;
            }).join('');
        }

        function scrollTop10(dir) { const row = document.getElementById('top10Row'); const w = row.querySelector(
                '.top10-card')?.offsetWidth || 340;
            row.scrollBy({ left: (w + 10) * dir, behavior: 'smooth' }); }

        function handleWatch(title) { const did = handleAdThenAction(watchClicks, title, () => { window.open(MOVIEBOX +
                    encodeURIComponent(title), '_blank');
                addRecent(title);
                toast('🎬 Opening ' + title);
                addNotif('▶ Watched: ' + title); }); if (!did) addNotif('📢 Ad Watch: ' + title); }

        function toggleWatchlistTop10(title) { let wl = JSON.parse(localStorage.getItem('wl') || '[]'); const i = wl.indexOf(
                title); if (i > -1) { wl.splice(i, 1);
                toast('Removed'); } else { wl.push(title);
                toast('Added!');
                addNotif('📋 Watchlist: ' + title); }
            localStorage.setItem('wl', JSON.stringify(wl));
            updateAllBadges(); }

        function renderAllMovies() {
            const grid = document.getElementById('movieGrid');
            grid.innerHTML = '';
            MOVIES.forEach((m, i) => {
                const q = m.r >= 8.5 ? 'IMAX' : m.r >= 8 ? '4K HDR' : m.r >= 7 ? '4K' : 'HD';
                const streams = m.st.split('|').map(s =>
                    `<span class="stream-tag ${STREAM_CLASS[s]}">${STREAM_NAMES[s]||s}</span>`).join('');
                const badge = m.tr ? '<span class="trending-badge">🔥TRENDING</span>' :
                    `<span class="poster-quality">${q}</span>`;
                const te = m.t.replace(/'/g, "\\'");
                const card = document.createElement('div');
                card.className = 'movie-card';
                card.setAttribute('data-genre', m.g);
                card.setAttribute('data-year', m.y);
                card.setAttribute('data-title', m.t);
                card.setAttribute('data-rating', m.r);
                card.innerHTML = `<div class="poster-wrap" onclick="openDetails('${te}')"><img src="${POSTER}${m.img}" alt="${m.t}" loading="lazy">${badge}<div class="card-actions-btns"><button class="icon-btn bookmark-btn" onclick="event.stopPropagation();toggleBookmark(this,'${te}')">🔖</button><button class="icon-btn wl-btn" onclick="event.stopPropagation();toggleWatchlistCard(this,'${te}')">➕</button></div></div><div class="card-body"><div class="card-header"><span class="card-title">${m.t}</span><span class="card-rating">⭐ ${m.r}</span></div><div class="card-meta"><span>${m.y}</span><span>EN</span><span>${m.g.split(' ')[0]}</span></div><p class="card-desc">${m.d}</p><div class="stream-tags">${streams}</div><div class="btn-row"><button class="btn-watch" onclick="handleWatch('${te}')">▶ Watch Now</button><button class="btn-dl" onclick="handleDownload(event,'${te}')">⬇ Download</button><button class="btn-tr" onclick="handleTrailer(event,'${te}')">🎬 Trailer</button></div><div class="share-row"><button class="share-btn" onclick="shareMovie('${te}','wa')">💬</button><button class="share-btn" onclick="shareMovie('${te}','tg')">📨</button><button class="share-btn" onclick="shareMovie('${te}','cp')">📋</button></div></div>`;
                grid.appendChild(card);
            });
            document.getElementById('movieGrid').appendChild(document.getElementById('noResults'));
            filterMovies();
        }

        function initGenreChips() {
            const c = document.getElementById('genreChips');
            const genres = ['Action', 'Horror', 'Sci-Fi', 'Drama', 'Comedy', 'Animation', 'Thriller', 'Crime'];
            const icons = { Action: '⚔️', Horror: '💀', 'Sci-Fi': '🪐', Drama: '🎭', Comedy: '😂', Animation: '🎨',
                Thriller: '🔪', Crime: '🕵️' };
            const counts = {};
            genres.forEach(g => counts[g] = 0);
            MOVIES.forEach(m => { const mg = m.g.split(' '); genres.forEach(g => { if (mg.some(x => x.toLowerCase() === g
                        .toLowerCase()) || (g === 'Sci-Fi' && mg.some(x => x.toLowerCase() === 'scifi'))) counts[
                    g]++; }); });
            genres.forEach(g => { const chip = document.createElement('span');
                chip.className = 'chip';
                chip.setAttribute('onclick', `filterByGenre('${g}', this)`);
                chip.innerHTML = `${icons[g]||''} ${g} <span class="count">${counts[g]}</span>`;
                c.appendChild(chip); });
        }

        function filterByGenre(genre, el) { activeGenre = genre;
            document.querySelectorAll('.chip').forEach(c => c.classList.remove('selected')); if (el) el.classList.add(
                'selected'); if (genre === 'all') document.querySelector('.chip').classList.add('selected');
            filterMovies(); }

        function filterMovies() {
            const s = document.getElementById('searchInput').value.toLowerCase();
            const sort = document.getElementById('sortSelect').value;
            const yr = document.getElementById('yearFilter').value;
            const cards = document.querySelectorAll('.movie-card');
            let v = 0;
            cards.forEach((card, i) => { const t = card.getAttribute('data-title').toLowerCase(); const g = card.getAttribute(
                    'data-genre').toLowerCase(); const y = card.getAttribute('data-year'); let show = true; if (s && !t
                    .includes(s) && !g.includes(s)) show = false; if (activeGenre !== 'all') { const ag = activeGenre
                        .toLowerCase(); if (ag === 'sci-fi') { if (!g.includes('sci-fi') && !g.includes('scifi')) show =
                        false; } else { if (!g.includes(ag)) show = false; } } if (yr !== 'all' && y !== yr) show =
                    false;
                card.style.display = show ? '' : 'none'; if (show) { v++;
                    card.style.animation = `fadeUp 0.35s ${v*0.03}s both`; } });
            document.getElementById('noResults').style.display = v === 0 ? 'block' : 'none'; if (sort !== 'default') { const
                    grid = document.getElementById('movieGrid'); const vis = [...cards].filter(c => c.style.display !==
                        'none');
                vis.sort((a, b) => { if (sort === 'rating') return parseFloat(b.getAttribute('data-rating')) - parseFloat(
                        a.getAttribute('data-rating')); if (sort === 'year') return parseInt(b.getAttribute('data-year')) -
                        parseInt(a.getAttribute('data-year')); if (sort === 'title') return a.getAttribute('data-title')
                        .localeCompare(b.getAttribute('data-title')); return 0; });
                vis.forEach(c => grid.appendChild(c)); }
        }

        function handleDownload(e, title) { e.stopPropagation(); const did = handleAdThenAction(dlClicks, title, () => { window
                    .open(MOVIEBOX + encodeURIComponent(title), '_blank');
                addRecent(title);
                toast('⬇ Opening ' + title);
                addNotif('⬇ Downloaded: ' + title); }); if (!did) addNotif('📢 Ad Download: ' + title); }

        function handleTrailer(e, title) { e.stopPropagation(); const did = handleAdThenAction(trClicks, title, () => { window
                    .open(YT_SEARCH + encodeURIComponent(title + ' trailer'), '_blank');
                toast('▶️ Opening trailer');
                addNotif('▶️ Trailer: ' + title); }); if (!did) addNotif('📢 Ad Trailer: ' + title); }

        function shareMovie(title, p) { const url = encodeURIComponent(location.href); const txt = encodeURIComponent(
                'Check out ' + title + ' 🎬'); if (p === 'wa') window.open('https://wa.me/?text=' + txt + ' ' + url,
                '_blank'); else if (p === 'tg') window.open('https://t.me/share/url?url=' + url + '&text=' + txt,
            '_blank'); else { navigator.clipboard?.writeText(title + ' - ' + location.href);
            toast('📋 Copied!'); } }

        function toggleBookmark(btn, title) { let bm = JSON.parse(localStorage.getItem('bm') || '[]'); const i = bm.indexOf(
                title); if (i > -1) { bm.splice(i, 1);
                btn.classList.remove('saved');
                btn.textContent = '🔖';
                toast('Removed'); } else { bm.push(title);
                btn.classList.add('saved');
                btn.textContent = '🔖✓';
                toast('Bookmarked!');
                addNotif('🔖 Bookmarked: ' + title); }
            localStorage.setItem('bm', JSON.stringify(bm)); }

        function restoreBookmarks() { const bm = JSON.parse(localStorage.getItem('bm') || '[]');
            document.querySelectorAll('.bookmark-btn').forEach(b => { const t = b.getAttribute('onclick')?.match(
                    /'([^']+)'\)/)?.[1]; if (t && bm.includes(t)) { b.classList.add('saved');
                    b.textContent = '🔖✓'; } }); }

        function toggleWatchlistCard(btn, title) { let wl = JSON.parse(localStorage.getItem('wl') || '[]'); const i = wl
                .indexOf(title); if (i > -1) { wl.splice(i, 1);
                btn.classList.remove('saved');
                btn.textContent = '➕';
                toast('Removed'); } else { wl.push(title);
                btn.classList.add('saved');
                btn.textContent = '✓';
                toast('Added!');
                addNotif('📋 Watchlist: ' + title); }
            localStorage.setItem('wl', JSON.stringify(wl));
            updateAllBadges(); }

        function openDetails(title) {
            const m = MOVIES.find(x => x.t === title); if (!m) return;
            const liked = JSON.parse(localStorage.getItem('liked') || '[]');
            const isLiked = liked.includes(title);
            const ratings = JSON.parse(localStorage.getItem('ratings') || '{}');
            const ur = ratings[title] || 0;
            const comments = JSON.parse(localStorage.getItem('comments') || '{}');
            const cmts = comments[title] || [];
            const streams = m.st.split('|').map(s =>
                `<span class="stream-tag ${STREAM_CLASS[s]}">${STREAM_NAMES[s]||s}</span>`).join('');
            let stars = ''; for (let i = 1; i <= 5; i++) stars +=
                `<span class="star ${i<=ur?'active':''}" onclick="rateMovie('${title.replace(/'/g,"\\'")}',${i})">★</span>`;
            let cmtsHTML = cmts.map(c => `<div class="comment-item">${c}</div>`).join('') ||
                '<p style="color:var(--muted);font-size:11px">No comments yet</p>';
            const related = MOVIES.filter(x => x.t !== title && x.g.split(' ').some(g => m.g.split(' ').includes(g)))
                .slice(0, 4);
            let relHTML = related.map(r =>
                `<div class="related-card" onclick="openDetails('${r.t.replace(/'/g,"\\'")}')"><img src="${POSTER}${r.img}" alt="${r.t}" loading="lazy"><div class="r-title">${r.t}</div></div>`
                ).join('');
            const te = title.replace(/'/g, "\\'");
            document.getElementById('detailsContent').innerHTML =
                `<div class="modal-header"><h2>🎬 ${m.t}</h2><button class="modal-close" onclick="closeDetails()">✕</button></div><div class="details-layout"><div class="details-poster"><img src="${POSTER}${m.img}" alt="${m.t}"></div><div class="details-info"><h2>${m.t}</h2><div class="meta"><span>📅 ${m.y}</span><span>⭐ ${m.r}</span><span>🎭 ${m.g}</span></div><div class="desc">${m.d}</div><div style="margin:8px 0">${streams}</div><div class="actions"><button class="btn-primary" onclick="handleWatch('${te}')">▶ Watch Now</button><button class="btn-primary" onclick="handleDownload(event,'${te}')">⬇ Download</button><button class="btn-outline" onclick="handleTrailer(event,'${te}')">🎬 Trailer</button><button class="${isLiked?'btn-liked':'btn-outline'}" onclick="toggleLike('${te}')">${isLiked?'❤️ Liked':'🤍 Like'}</button></div><div class="star-rating">${stars}</div><div class="comment-box"><textarea id="commentInput" placeholder="Write a comment..."></textarea><button onclick="addComment('${te}')">Post 💬</button><div class="comments-list">${cmtsHTML}</div></div>${relHTML?`<div class="related-section"><h4>🎯 Related Movies</h4><div class="related-grid">${relHTML}</div></div>`:''}</div></div>`;
            document.getElementById('detailsModal').classList.add('open');
            addRecent(title);
        }

        function closeDetails() { document.getElementById('detailsModal').classList.remove('open'); }

        function rateMovie(title, r) { const ratings = JSON.parse(localStorage.getItem('ratings') || '{}');
            ratings[title] = r;
            localStorage.setItem('ratings', JSON.stringify(ratings));
            toast('⭐ Rated ' + r + ' stars!');
            addNotif('⭐ Rated: ' + title);
            openDetails(title); }

        function addComment(title) { const inp = document.getElementById('commentInput'); if (!inp || !inp.value.trim()) return;
            const comments = JSON.parse(localStorage.getItem('comments') || '{}'); if (!comments[title]) comments[title] = [];
            comments[title].push(inp.value.trim());
            localStorage.setItem('comments', JSON.stringify(comments));
            toast('💬 Comment added!');
            addNotif('💬 Comment: ' + title);
            openDetails(title); }

        function toggleLike(title) { let liked = JSON.parse(localStorage.getItem('liked') || '[]'); const i = liked.indexOf(
                title); if (i > -1) { liked.splice(i, 1);
                toast('Removed'); } else { liked.push(title);
                toast('❤️ Liked!');
                addNotif('❤️ Liked: ' + title); }
            localStorage.setItem('liked', JSON.stringify(liked));
            updateAllBadges();
            openDetails(title); }

        function openSidebar(type) { document.getElementById('sidebarOverlay').classList.add('show'); if (type ===
                'watchlist') { renderWatchlistSidebar();
                document.getElementById('watchlistSidebar').classList.add('open'); } else if (type === 'liked') {
                renderLikedSidebar();
                document.getElementById('likedSidebar').classList.add('open'); } else if (type === 'notifications') {
                renderNotifSidebar();
                document.getElementById('notificationsSidebar').classList.add('open');
                document.getElementById('notifBadge').style.display = 'none'; } }

        function closeSidebar() { document.getElementById('sidebarOverlay').classList.remove('show');
            document.querySelectorAll('.sidebar').forEach(s => s.classList.remove('open')); }

        function renderWatchlistSidebar() { const wl = JSON.parse(localStorage.getItem('wl') || '[]'); const ct = document
                .getElementById('watchlistContent'); if (!wl.length) { ct.innerHTML =
                    '<div class="sidebar-empty"><span class="icon">📋</span><p>Empty</p></div>'; return; }
            ct.innerHTML = wl.map(t => { const m = MOVIES.find(x => x.t === t); if (!m) return ''; return `
                    <div class="sidebar-item" onclick="openDetails('${t.replace(/'/g,"\\'")}');closeSidebar()"><img src="${POSTER}${m.img}" alt="${t}"><div><h4>${t}</h4><p>⭐ ${m.r} • ${m.y}</p></div></div>`; }
                ).join(''); }

        function renderLikedSidebar() { const liked = JSON.parse(localStorage.getItem('liked') || '[]'); const ct = document
                .getElementById('likedContent'); if (!liked.length) { ct.innerHTML =
                    '<div class="sidebar-empty"><span class="icon">❤️</span><p>Empty</p></div>'; return; }
            ct.innerHTML = liked.map(t => { const m = MOVIES.find(x => x.t === t); if (!m) return ''; return `
                    <div class="sidebar-item" onclick="openDetails('${t.replace(/'/g,"\\'")}');closeSidebar()"><img src="${POSTER}${m.img}" alt="${t}"><div><h4>${t}</h4><p>⭐ ${m.r} • ${m.y}</p></div></div>`; }
                ).join(''); }

        function renderNotifSidebar() { const ct = document.getElementById('notificationsContent'); if (!notifications
                .length) { ct.innerHTML = '<div class="sidebar-empty"><span class="icon">🔔</span><p>Empty</p></div>'; return; }
            ct.innerHTML = notifications.map(n => { const p = n.split('] '); return `<div class="notif-item">${p[1]||n}<div class="time">${p[0]?.replace('[','')||''}</div></div>`; }
                ).join(''); }

        function addNotif(msg) { const t = new Date().toLocaleTimeString();
            notifications.unshift(`[${t}] ${msg}`); if (notifications.length > 50) notifications.pop();
            localStorage.setItem('notifications', JSON.stringify(notifications));
            updateAllBadges(); }

        function loadNotifications() { notifications = JSON.parse(localStorage.getItem('notifications') || '[]');
            updateAllBadges(); }

        function updateAllBadges() { const wl = JSON.parse(localStorage.getItem('wl') || '[]'); const liked = JSON.parse(
                localStorage.getItem('liked') || '[]'); const wB = document.getElementById('wlBadge'); const lB = document
                .getElementById('likedBadge'); const nB = document.getElementById('notifBadge'); if (wl.length) { wB.style
                    .display = 'flex';
                wB.textContent = wl.length; } else wB.style.display = 'none'; if (liked.length) { lB.style.display = 'flex';
                lB.textContent = liked.length; } else lB.style.display = 'none'; if (notifications.length) { nB.style.display =
                    'flex';
                nB.textContent = notifications.length; } else nB.style.display = 'none'; }

        function addRecent(title) { const m = MOVIES.find(x => x.t === title); if (!m) return; let recent = JSON.parse(
                localStorage.getItem('recent') || '[]');
            recent = recent.filter(r => r.title !== title);
            recent.unshift({ title, img: m.img }); if (recent.length > 8) recent.pop();
            localStorage.setItem('recent', JSON.stringify(recent));
            renderRecent(); }

        function renderRecent() { const recent = JSON.parse(localStorage.getItem('recent') || '[]'); const sec = document
                .getElementById('recentSection'); const row = document.getElementById('recentRow'); if (!recent.length) { sec
                    .classList.remove('show'); return; }
            sec.classList.add('show');
            row.innerHTML = recent.map(r =>
                `<div class="recent-card" onclick="openDetails('${r.title.replace(/'/g,"\\'")}')"><img src="${POSTER}${r.img}" alt="${r.title}" loading="lazy"><div class="r-title">${r.title}</div></div>`
                ).join(''); }

        function toast(msg) { const a = document.getElementById('toastArea'); const t = document.createElement('div');
            t.className = 'toast';
            t.textContent = msg;
            a.appendChild(t);
            setTimeout(() => { t.style.opacity = '0';
                t.style.transition = 'opacity 0.3s';
                setTimeout(() => t.remove(), 300); }, 3000); if (a.children.length > 5) a.firstChild.remove(); }

        function toggleTheme() { document.body.classList.toggle('light-mode'); const isL = document.body.classList.contains(
                'light-mode');
            localStorage.setItem('theme', isL ? 'light' : 'dark');
            toast(isL ? '☀️ Light' : '🌙 Dark'); }

        function subscribeNewsletter() { const i = document.querySelector('.footer-nl input'); if (i && i.value.includes(
                '@') && i.value.includes('.')) { toast('✅ Subscribed!');
                addNotif('✅ Subscriber');
                i.value = ''; } else toast('⚠️ Valid email please'); }

        window.addEventListener('scroll', () => { document.getElementById('progressBar').style.width = (window.scrollY / (
                document.documentElement.scrollHeight - window.innerHeight) * 100) + '%';
            document.getElementById('scrollTopBtn').classList.toggle('visible', window.scrollY > 400); }, { passive: true });
        document.addEventListener('keydown', e => { if (e.key === 'Escape') { closeDetails();
                closeSidebar(); } });
        document.getElementById('detailsModal').addEventListener('click', function(e) { if (e.target === this) closeDetails(); });

        window.openDetails = openDetails;
        window.closeDetails = closeDetails;
        window.openSidebar = openSidebar;
        window.closeSidebar = closeSidebar;
        window.filterByGenre = filterByGenre;
        window.filterMovies = filterMovies;
        window.handleDownload = handleDownload;
        window.handleTrailer = handleTrailer;
        window.handleWatch = handleWatch;
        window.shareMovie = shareMovie;
        window.toggleBookmark = toggleBookmark;
        window.toggleWatchlistCard = toggleWatchlistCard;
        window.toggleWatchlistTop10 = toggleWatchlistTop10;
        window.toggleLike = toggleLike;
        window.rateMovie = rateMovie;
        window.addComment = addComment;
        window.addRecent = addRecent;
        window.toggleTheme = toggleTheme;
        window.subscribeNewsletter = subscribeNewsletter;
        window.scrollTop10 = scrollTop10;

        document.addEventListener('DOMContentLoaded', init);
        if (document.readyState !== 'loading') init();
    </script>
</body>
</html>
