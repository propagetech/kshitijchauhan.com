You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "Kshitij Chauhan | Blogs",
      "first_heading": "Piano Concerts during COVID times"
    }
  },
  {
    "path": "blog_notorious-lolipop---loving-more-than-self.html",
    "context": {
      "title": "Notorious Lolipop - Loving more than self",
      "first_heading": "Notorious Lolipop - Loving more than self"
    }
  },
  {
    "path": "blog_piano-concerts-during-covid-times.html",
    "context": {
      "title": "Piano Concerts during COVID times",
      "first_heading": "Piano Concerts during COVID times"
    }
  },
  {
    "path": "blog_time-is-everything---quarantino.html",
    "context": {
      "title": "Time is everything - Quarantino",
      "first_heading": "Time is everything - Quarantino"
    }
  },
  {
    "path": "blog_victory-in-the-face-of-adversity.html",
    "context": {
      "title": "Victory In The Face Of Adversity",
      "first_heading": "Victory In The Face Of Adversity"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/614da49ccb4f3fae8d700f8236e5531a.css",
    "context": {
      "path": "css/614da49ccb4f3fae8d700f8236e5531a.css"
    }
  },
  {
    "path": "css/90c9c6e1e997f909ee71110a5d887998.css",
    "context": {
      "path": "css/90c9c6e1e997f909ee71110a5d887998.css"
    }
  },
  {
    "path": "css/923d7a12989d8629b2276bcb808c92b9.css",
    "context": {
      "path": "css/923d7a12989d8629b2276bcb808c92b9.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/9e78a9df7c3f211b97abb945170ccdbd.css",
    "context": {
      "path": "css/9e78a9df7c3f211b97abb945170ccdbd.css"
    }
  },
  {
    "path": "css/ad41e28bdcede3df8615e30d2b7622a3.css",
    "context": {
      "path": "css/ad41e28bdcede3df8615e30d2b7622a3.css"
    }
  },
  {
    "path": "css/c106b025e7e6b2ed84578135d4c38342.css",
    "context": {
      "path": "css/c106b025e7e6b2ed84578135d4c38342.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0716f0e0259f1643675bab93d80dbfc1.webp",
    "context": {
      "refs": [
        {
          "alt": "books",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09cacaf194ec85a0fcc7b4aa39d92524.webp",
    "context": {
      "refs": [
        {
          "alt": "Time is everything - Quarantino",
          "title": ""
        },
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29ee094b97078165470a5a7b45d957f6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30ab838fe29bbebe50efa4b19a890dba.webp",
    "context": {
      "refs": [
        {
          "alt": "Piano during COVID times",
          "title": ""
        },
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7637c7498c8796dfb8e60101bd449303.webp",
    "context": {
      "refs": [
        {
          "alt": "mymusic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7cc890bc2c0f40b90463c02b596aaa4a.webp",
    "context": {
      "refs": [
        {
          "alt": "Its my life - Bon Jovi",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/804592d28a1aaf0b3aef69532e262589.webp",
    "context": {
      "refs": [
        {
          "alt": "Notorious Lolipop - Loving more than self",
          "title": ""
        },
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a30296837f86df6a83f31c9966f71685.webp",
    "context": {
      "refs": [
        {
          "alt": "Victory In The Face Of Adversity",
          "title": ""
        },
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a39bcabc616dab36f26346454b1ded0b.webp",
    "context": {
      "refs": [
        {
          "alt": "about",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ccc1dcdd8f8614ce672b77128f27fc60.webp",
    "context": {
      "refs": [
        {
          "alt": "Faded by Alan Walker",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfdff53bc78fb106f99ee8f28b2576de.webp",
    "context": {
      "refs": [
        {
          "alt": "F\u00fcr Elise (Beethoven) in six flavors",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e087fb7efca97977b41c86d58b3d7af4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f5dbfbeaed89ec120f7f53b8fd0beaa3.webp",
    "context": {
      "refs": [
        {
          "alt": "Rondo Alla Turca (Turkish March) - Mozart",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Kshitij Chauhan | I am a music enthusiast and I love to play tales on piano",
      "first_heading": "I am amusicenthusiast and I love to playtaleson piano"
    }
  },
  {
    "path": "js/024c2427a07d4754d082b32ff6f47796.js",
    "context": {
      "path": "js/024c2427a07d4754d082b32ff6f47796.js"
    }
  },
  {
    "path": "js/027151cf1be95681de1b467942001858.js",
    "context": {
      "path": "js/027151cf1be95681de1b467942001858.js"
    }
  },
  {
    "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js",
    "context": {
      "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js"
    }
  },
  {
    "path": "js/2d36e9fa24b491802cf18f39a308190c.js",
    "context": {
      "path": "js/2d36e9fa24b491802cf18f39a308190c.js"
    }
  },
  {
    "path": "js/2d62c5e761d3e1992478716162667ce5.js",
    "context": {
      "path": "js/2d62c5e761d3e1992478716162667ce5.js"
    }
  },
  {
    "path": "js/328ee378638a24926abf5dec969f9194.js",
    "context": {
      "path": "js/328ee378638a24926abf5dec969f9194.js"
    }
  },
  {
    "path": "js/3e734a79111d3ae5022fadd97f4b4570.js",
    "context": {
      "path": "js/3e734a79111d3ae5022fadd97f4b4570.js"
    }
  },
  {
    "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js",
    "context": {
      "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js"
    }
  },
  {
    "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js",
    "context": {
      "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js"
    }
  },
  {
    "path": "js/4a184d88eb9269b7dbce11b716f40379.js",
    "context": {
      "path": "js/4a184d88eb9269b7dbce11b716f40379.js"
    }
  },
  {
    "path": "js/56848c032b05f79a1c67ea6d7b451252.js",
    "context": {
      "path": "js/56848c032b05f79a1c67ea6d7b451252.js"
    }
  },
  {
    "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js",
    "context": {
      "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js"
    }
  },
  {
    "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js",
    "context": {
      "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js"
    }
  },
  {
    "path": "js/6432203ce192bdda9fff6890193487b5.js",
    "context": {
      "path": "js/6432203ce192bdda9fff6890193487b5.js"
    }
  },
  {
    "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js",
    "context": {
      "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js"
    }
  },
  {
    "path": "js/7d7d8ec406a653220337bde42ddcd998.js",
    "context": {
      "path": "js/7d7d8ec406a653220337bde42ddcd998.js"
    }
  },
  {
    "path": "js/969912c5e1cdd73b7812defd4dbd0119.js",
    "context": {
      "path": "js/969912c5e1cdd73b7812defd4dbd0119.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js",
    "context": {
      "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js"
    }
  },
  {
    "path": "js/aeea5981f09059b3304ead8b513e8042.js",
    "context": {
      "path": "js/aeea5981f09059b3304ead8b513e8042.js"
    }
  },
  {
    "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js",
    "context": {
      "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js"
    }
  },
  {
    "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js",
    "context": {
      "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js"
    }
  },
  {
    "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js",
    "context": {
      "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js"
    }
  },
  {
    "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js",
    "context": {
      "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js"
    }
  },
  {
    "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js",
    "context": {
      "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js"
    }
  },
  {
    "path": "js/e83b51d598b2a45483252c3be82d77b0.js",
    "context": {
      "path": "js/e83b51d598b2a45483252c3be82d77b0.js"
    }
  },
  {
    "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js",
    "context": {
      "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js"
    }
  },
  {
    "path": "js/f5b6708cffe7c1147c483017fbec7d58.js",
    "context": {
      "path": "js/f5b6708cffe7c1147c483017fbec7d58.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.