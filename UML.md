```uml
classDiagram

    %% Main Classes
    class a_mjava {
        +tz(): void
    }

    class bfq2_iyu {
        -Video player UI
        -WebView component
        -URL input
        -Play controls
    }

    class byusi_myu {
        +ztl(): void
    }

    class core_myu {
        +list(): void
        +uigo(): void
    }

    class dir_iyu {
        -Directory browser
        -Refresh control
        -File list
    }

    class hlist_iyu {
        -File list item
        -File type icons
        -Click handlers
    }

    class home_iyu {
        -Main screen
        -Navigation
        -File browser
    }

    class login_iyu {
        -Login form
        -Email/password
        -Captcha
    }

    class Lottie_myu {
        +loaddex(): void
        +setImageLottie()
        +startLottie()
    }

    class webView_mjava {
        +setUa(): void
        +getUa(): String
    }

    %% Relationships
    home_iyu --> core_myu : uses
    home_iyu --> dir_iyu : contains
    dir_iyu --> hlist_iyu : contains
    dir_iyu --> core_myu : uses
    core_myu --> byusi_myu : uses
    bfq2_iyu --> a_mjava : uses
    login_iyu --> Lottie_myu : uses
    note for login_iyu "Uses Lottie for animations"
    note for bfq2_iyu "Video player interface"
    note for core_myu "Core business logic"
```