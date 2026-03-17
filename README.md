# TheCatAPI - iOS SwiftUI

[![Swift Version](https://img.shields.io/badge/Swift-5.0-orange.svg)](https://swift.org)
[![Platform](https://img.shields.io/badge/platform-iOS-lightgrey.svg)](https://developer.apple.com/ios/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## The Same Project with UIKit Framework

🛠 The Same Project Built with UIKit
You can also check out the UIKit version of this project here: TheCatAPIUIKit Repo (https://github.com/JoNaLac/PragmaUIKit)

## Descripción

Una aplicación iOS nativa desarrollada con SwiftUI que consume la API de [TheCatAPI](https://thecatapi.com/) para mostrar información sobre razas de gatos, permitiendo marcar favoritos y explorar detalles de cada raza.

## Arquitectura

Esta aplicación fue desarrollada siguiendo el patrón de arquitectura **MVVM (Model-View-ViewModel)**:

- **Model**: Entidades y modelos de datos
- **View**: Interfaces de usuario construidas con SwiftUI
- **ViewModel**: Lógica de negocio y estado de la aplicación
- **Services**: Capa de acceso a datos y API

## Patrones de Diseño

- **Observer Pattern**: Implementado a través de ObservableObject para la comunicación View-ViewModel
- **Repository Pattern**: Para el acceso a datos
- **Dependency Injection**: Para facilitar el testing y modularidad
- **Factory Pattern**: Creación de objetos complejos

## Tecnologías y Herramientas

- 📱 SwiftUI
- 🔄 Combine Framework
- 🗄️ SwiftData para persistencia
- 🌐 URLSession para networking
- 🧪 XCTest para testing

## Requisitos

- iOS 18.2+
- Xcode 16.2+
- Swift 5.0+

## Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/Rawstells/PragmaSwiftUI.git
```

2. Abre el archivo `.xcodeproj` en Xcode

3. Configura tu API key de TheCatAPI en `CatAPIService.swift`
```swift
private let apiKey = "TU_API_KEY" // Obtén tu API key en https://thecatapi.com/
```

4. Compila y ejecuta la aplicación

## Características

- **Exploración de Razas**: Lista paginada de razas de gatos
- **Búsqueda**: Filtrado de razas por nombre
- **Detalle**: Información detallada de cada raza, incluyendo:
  - Características físicas y comportamentales
  - Niveles de adaptabilidad, afecto, energía, etc.
  - Imágenes y origen
- **Favoritos**: Gestión de razas favoritas con persistencia local
- **Enlaces Externos**: Acceso a información adicional vía Wikipedia

## Estructura del Proyecto

```
📦 TheCatAPISwiftUI  
├── 📂 Framework  
│   ├── 📄 ImageManager  
│   ├── 📄 ImageLoader  
│   ├── 📄 RequestManager  
│   ├── 📄 APIManager  
│   ├── 📄 ErrorCases  
│   └── 📄 WebService  
│  
├── 📂 Main  
│   ├── 📄 TheCatAPISwiftUIApp  
│   ├── 📂 Preview Content  
│   └── 📂 Preview Assets  
│  
├── 📂 Resources  
│   ├── 📂 Assets (Íconos/Imágenes)  
│   └── 📂 GIFs (Animaciones)  
│  
├── 📂 Sections  
│   ├── 📂 BreedDetail  
│   │   ├── 📂 View  
│   │   │   ├── 📄 BreedDetailView  
│   │   │   └── 📄 BreedCharacteristicsView  
│   │   └── 📂 ViewModel  
│   │       ├── 📄 BreedDetailViewModel  
│   │       └── 📄 BreedCharacteristicsViewModel  
│   │  
│   └── 📂 BreedsList  
│       ├── 📂 Model  
│       │   ├── 📄 Breed  
│       │   ├── 📄 BreedImagesModel  
│       │   └── 📄 BreedModel  
│       ├── 📂 View  
│       │   ├── 📄 BreedCardView  
│       │   └── 📄 BreedsListView  
│       └── 📂 ViewModel  
│           ├── 📄 BreedsViewModel  
│           └── 📄 CardViewModel  
│  
├── 📂 Favorites  
│   ├── 📂 View  
│   │   ├── 📄 FavoriteCardView  
│   │   └── 📄 FavoritesView  
│   ├── 📄 FavoritesViewManager  
│   └── 📄 FavoritesViewModel  
│  
├── 📄 MainTabView  
├── 📄 SplashView  
└── 📂 Utils (Helpers/Extensions)
```

## API

La aplicación consume [TheCatAPI](https://thecatapi.com/), que proporciona:

- Listado de razas con información detallada
- Imágenes de gatos por raza
- Sistema de favoritos
- Búsqueda y filtrado

## Testing

El proyecto incluye tests unitarios para garantizar la calidad del código:

```bash
# Ejecutar tests
xcodebuild test -scheme PragmaSwiftUI -destination 'platform=iOS Simulator,name=iPhone 13'
```

## Autor

Desarrollado por [@JoNaLac](https://github.com/JoNaLac)

## Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

*Nota: Este proyecto fue desarrollado como parte de una prueba técnica para Pragma.*
