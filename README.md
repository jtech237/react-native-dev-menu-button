# React Native Dev Menu

Un bouton flottant de développement avec menu d'actions pour React Native.

## 🚀 Installation

```bash
npm install react-native-dev-button
# or
yarn add react-native-dev-button
```

## Dépendances requises

```bash
npm install @react-native-async-storage/async-storage
# ou
yarn add @react-native-async-storage/async-storage
```

## 📱 Utilisation de base

```tsx
import React from 'react';
import {View} from 'react-native';
import {DevButton} from 'react-native-dev-button';

export default function App() {
    return (
        <View style={{flex: 1}}>
            {/* Votre app */}

            {__DEV__ && (
                <DevButton
                    position="bottom-right"
                    accentColor="#e74c3c"
                />
            )}
        </View>
    );
}
```

## 🎨 Personnalisation

### Actions personnalisées

```tsx
import {DevButton, MenuAction} from 'react-native-dev-button';
import Icon from 'react-native-vector-icons/MaterialIcons';

const customActions: MenuAction[] = [
    {
        label: 'Reset App State',
        icon: {
            component: Icon,
            name: 'refresh',
            color: '#3498db'
        },
        onPress: () => {
// Votre logique de reset
        }
    }
];

<DevButton customActions={customActions}/>
```

## 📚 Documentation complète

Voir [API.md]() pour la documentation complète.

## 📄 License

[MIT]()
