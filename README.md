
# Конспект по Expo

> **Expo** - это фреймворк React Native, который облегчает разработку приложений для Android и iOS. 

---

## Create a project (Создание проекта)

### Системные требования 

Node.js (LTS).
поддерживаются macOS, Windows (Powershell и WSL 2) и Linux.

### Создание проекта

Для создания нового проекта искользуется команда: npx create-expo-app@latest

Вместо стандартного проекта можно начать с одного из примеров Expo. Это небольшие приложения, каждое из которых демонстрирует определённую функцию или интеграцию, такие как Expo Router, Expo Widgets или экран камеры.

Чтобы просмотреть полный список и выбрать интерактивно, запустите с помощью create-expo-app--example Опция и Нет имени:
npx create-expo-app@latest --example

Чтобы создать известный пример напрямую, передайте его имя:
npx create-expo-app@latest --example with-widgets

### Настройте агента ИИ

Новый проект включает AGENTS.md с контекстом проекта для ИИ-агентов. При установке Claude Code также включает .claude/settings.json для включения плагина Expo. Claude Code и Codex имеют официальный плагин для Expo. Используя одну команду, вы можете установить Expo Skills и зарегистрировать сервер Expo Model Context Protocol (MCP):
claude plugin install expo@claude-plugins-official

Затем пройдите внутрь сессии Claude Code и войдите в свой аккаунт Expo./mcp

---

## Start developing (Начало разработки)

### Запуск сервера разработки

Чтобы запустить сервер разработки, выполните следующую команду:
npx expo start

### Открытие приложение на вашем устройстве

После выполнения вышеуказанной команды вы увидите QR-код в терминале. Отсканируйте этот QR-код, чтобы открыть приложение на вашем устройстве.

Если вы используете эмулятор Android или iOS Simulator, вы можете нажать или соответственно, чтобы открыть приложение.AI

### Первые изменение

Сделайте первое изменение
Откройте файл src/app/index.tsx в редакторе кода и внесите изменения.

     <ThemedView style={styles.heroSection}>
       <AnimatedIcon />
 <ThemeText type="title" style={styles.title}>
 Добро пожаловать в&nbsp; Экспо
 Привет, мир!
       </ThemedText>
     </ThemedView>

---

## Next steps

### Сбросьте проект
Вы можете убрать стандартный код и начать новый проект. Выполните следующую команду для сброса проекта:
npm run reset-project
Эта команда переместит существующие файлы в приложении в app-example, затем создаёт новую папку приложения с новым файлом index.tsx.

### Разработка, обзор и развертывание
Узнайте, как развиваться, читая документацию в разделе «Разработка». Вы научитесь создавать элементы интерфейса, добавлять модульные тесты, включать нативные модули и многое другое.

---

## Tools for development (Инструменты для разработки)

### Expo CLI

Expo CLI — это инструмент разработки, который устанавливается автоматически вместе с пакетом при создании нового проекта. Вы можете использовать его, используя (Node.js package runner).exponpx

Он создан для того, чтобы помочь вам быстрее двигаться на этапе разработки приложения. Например, ваше первое взаимодействие с Expo CLI — это запуск сервера разработки с помощью команды: .npx expo start

Ниже приведён список распространённых команд, которые вы будете использовать с Expo CLI при разработке приложения:

- npx expo start - Запускает сервер разработки (независимо от того, используете ли вы билд для разработки или Expo Go)

- npx expo prebuild - Генерирует нативные каталоги для Android и iOS с помощью Prebuild

- npx expo run:android - Компилирует нативное Android-приложение локально

- npx expo run:ios - Компилирует нативное iOS-приложение локально

- npx expo install package-name - Раньше устанавливали новую библиотеку или проверяли и обновляли конкретные библиотеки в вашем проекте, добавляя опцию к этой команде.--fix

- npx expo lint - Настройка и настройки ESLint. Если ESLint уже настроен, эта команда уничтожит файлы проекта

### EAS CLI

EAS CLI используется для входа в ваш аккаунт Expo и компиляции приложения с помощью различных сервисов EAS, таких как Build, Update или Submit. Вы также можете использовать этот инструмент, чтобы:

- Опубликуйте своё приложение в магазинах приложений

- Создайте разработку, превью или продакшн для вашего приложения

- Создание обновлений по эфиру (OTA)

- Управляйте учетными данными вашего приложения

- Создайте ad hoc профиль для устройства iOS

- Чтобы использовать EAS CLI, нужно установить его глобально на вашем локальном компьютере, выполнив команду:
npm install --global eas-cli

### Expo Doctor

Expo Doctor — это инструмент командной строки, используемый для диагностики проблем в вашем проекте Expo. Чтобы воспользоваться им, выполните следующую команду в корневой директории вашего проекта:
npx expo-doctor

Эта команда выполняет проверки и анализ кодовой базы вашего проекта на предмет распространённых проблем с конфигурацией приложения и файлами package.json, совместимостью зависимостей, конфигурационными файлами и общим состоянием проекта. После завершения проверки Expo Doctor публикует результаты

### Orbit

Orbit — это приложение для macOS, Windows и Linux, которое позволяет:

- Устанавливайте и запускайте сборки с EAS на физических устройствах и эмуляторах

- Устанавливайте и запускайте обновления от EAS на эмуляторах Android или симуляторах iOS

- Запускайте проекты с закусками на эмуляторах Android или симуляторах iOS

- Используйте локальные файлы для установки и запуска приложений. Orbit поддерживает любые Android apk, совместимые с iOS Simulator .app или специальные подписанные приложения

- Посмотрите список закреплённых проектов на вашей панели управления EAS

Вы можете скачать Orbit с Homebrew для macOS или напрямую с релизов на GitHub
brew install expo-orbit

### Expo Tools для VS Code

Expo Tools — это расширение VS Code, которое улучшает опыт разработки при работе с конфигурационными файлами приложений. Он предоставляет такие функции, как автозаполнение и intellisense для файлов, таких как конфигурация приложений, конфигурация EAS, конфигурация хранилища и конфигурации модуля Expo.

Вы также можете использовать его для отладки приложения с помощью встроенного отладчика VS Code, чтобы устанавливать точки остановки, проверять переменные, выполнять код через отладочную консоль и многое другое. См. раздел «Отладка с помощью VS Code» для того, как использовать это расширение для отладки.

### Испытание прототипов с Snack и Expo Go

#### Snack

Snack — это встроенная среда разработки, работающая аналогично Expo Go. Это отличный способ делиться фрагментами кода и экспериментировать с React Native, не скачивая инструменты на компьютер.

Чтобы воспользоваться им, зайдите в snack.expo.dev, отредактируйте компонент в App.js, выберите платформу (Android, iOS или веб) в правой панели и посмотрите изменения в реальном времени.<Text>

#### Expo Go
Expo Go — это бесплатная открытая площадка для студентов и учащихся, чтобы попробовать React Native. Он работает на Android и iOS.

##### expo-go CLI
The expo-go CLI это автономный инструмент, который скачает бинарный файл Expo Go для платформы и конкретной версии SDK или печатает его URL для загрузки. Передайте версию SDK для закрепления конкретного релиза или опустите её для последнего релиза и укажите платформу для загрузки правильного бинарного файла

npx expo-go download android latest

npx expo-go url ios latest

Эта команда загружает приложение Expo Go в текущий каталог и кэширует его в ~/.expo.

### каталог React Native
Любая библиотека, совместимая с React Native, работает в проекте Expo, когда вы используете build для создания проекта.

reactnative.directory — это поисковая база данных библиотек React Native. Если библиотека, которую вы ищете, не включена в Expo SDK, используйте каталог, чтобы найти совместимую библиотеку для вашего проекта.

---

## Почему приложениям React Native нужна навигационная библиотека

Core React Native включает базовые компоненты интерфейса, сенсорную обработку, API устройств и сетевую систему, но исключает, среди прочего, хранилище, камеру, карты, большинство датчиков устройств и навигацию! Они предназначены для покрытия общественными библиотеками.

### React Navigation

React Navigation — это навигационная библиотека на основе компонентов, широко используемая в экосистеме React Native. Он позволяет компоназировать навигаторы стека, вкладок и ящиков полностью в коде, чтобы реализовать сложные потоки, пользовательские переходы и специфичные для приложения UX-паттерны.

Библиотека предлагает платформенно-специфический визуальный стиль с плавными анимациями и жестами, унифицированную мобильную и веб-маршрутизацию, автоматические глубокие ссылки, типографические маршруты со статической конфигурацией и высоко настраиваемые.

### Expo Router (рекомендуется для выставочных проектов)

Expo Router — это файловая библиотека маршрутизации для проектов Expo и React Native. Следуя правилам каталога приложений, файлы превращаются в маршруты и интегрируются с Expo for Expo CLI и пакетированием без дополнительной настройки. Библиотека также добавляет такие функции, как типизированные маршруты, динамические маршруты, ленивое объединение в разработке, статическое рендеринг для веба и автоматическое глубокое ссылание.

Новые проекты Expo, созданные с помощью Expo Router по умолчанию.npx create-expo-app@latest

---

# Конспект по Expo tutorial

## Create your first app (Создайте своё первое приложение)

### Инициализация нового приложения Expo

Мы используем create-expo-app чтобы инициализировать новое приложение Expo. Это командный инструмент для создания нового проекта React Native. Выполните следующую команду в терминале:
npx create-expo-app@latest StickerSmash
Select an Expo SDK version > SDK 57
cd StickerSmash

Эта команда создаст новую папку проекта под названием StickerSmash, используя шаблон по умолчанию. Этот шаблон содержит необходимый шаблонный код и библиотеки, необходимые для создания нашего приложения, включая Expo Router, и позволяет нам тестировать приложение с установленным Expo Go на наших устройствах. Мы продолжим добавлять новые библиотеки в этом учебнике по мере необходимости.

### Запустить скрипт reset-project

Давайте запустим скрипт, чтобы удалить шаблонный код:
npm run reset-project

После выполнения вышеуказанной команды в папке src/app остаются два файла (index.tsx и _layout.tsx). Предыдущие файлы из каталога src (включая компоненты, константы и крючки) перемещаются внутри папки примера скриптом. По ходу работы мы будем создавать собственные каталоги и компонентные файлы.

### Запустите приложение на мобильных устройствах и веб

В каталоге проекта выполните следующую команду, чтобы запустить сервер разработки из терминала:
npx expo start

После выполнения вышеуказанной команды:
Сервер разработки запустится, и вы увидите QR-код внутри окна терминала.
Отсканируйте этот QR-код, чтобы открыть приложение на устройстве. На Android используйте опцию QR-кода Expo Go > Scan. На iOS используйте стандартное приложение камеры.
Чтобы запустить веб-приложение, нажмите в терминале. Веб-приложение откроется в браузере по умолчанию.W

### Редактировать экран индекса

Файл src/app/index.tsx определяет текст, отображаемый на экране приложения. Это входная точка нашего приложения и запускается при запуске сервера разработки. Он использует основные компоненты React Native, такие как и для отображения фона и текста.<View><Text>

Стили, применяемые к этим компонентам, используют объекты JavaScript, а не CSS, который используется в вебе. Однако многие свойства будут казаться знакомыми. Большинство компонентов React Native принимают проп, который принимает объект JavaScript в качестве своего значения.

Давайте изменим экран src/app/index.tsx:

1. Импортируйте из и создайте объект для определения наших пользовательских стилей.StyleSheetreact-nativestyles
2. Добавьте свойство с значением . Это меняет цвет фона.styles.container.backgroundColor<View>#25292e
3. Замените значение по умолчанию на «Главный экран».<Text>
4. Добавьте свойство с значением (белый) для изменения цвета текста.styles.text.color<Text>#fff
src/app/index.tsx

import {Text, View, StyleSheet } from 'react-native';

export default function Index() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Home screen</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    color: '#fff',
  },
});

---

## Добавление навигации

### Основы Expo Router

Expo Router — это фреймворк маршрутизации на основе файлов для React Native и веб-приложений. Он управляет навигацией между экранами и использует одни и те же компоненты на нескольких платформах. Чтобы начать, нам нужно знать о следующих конвенциях:

- Каталог приложений: Специальная директория, содержащая только маршруты и их макеты. Любые файлы, добавленные в эту директорию, становятся экраном внутри нашего нативного приложения и страницей в интернете. В стандартном шаблоне он расположен на src/app.
- Корневая верстка: файл src/app/_layout.tsx. Он определяет общие элементы интерфейса, такие как заголовки и панели вкладок, чтобы они были согласованы между разными маршрутами.
- Правила имён файлов: Имена индексных файлов, такие как index.tsx, совпадают с родительским каталогом и не добавляют сегмент пути. Например, файл index.tsx в каталоге src/app совпадает с маршрутом./
- Файл маршрута экспортирует компонент React в качестве своего значения по умолчанию. Он может использовать либо , , , либо расширение..js.jsx.ts.tsx
- Android, iOS и веб имеют единую навигационную структуру.

### 1 Добавьте новый экран в стек

Давайте создадим новый файл с названием about.tsx внутри папки src/app. При навигации пользователя по маршруту отображается имя экрана./about

import { Text, View, StyleSheet } from 'react-native';

export default function AboutScreen() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>About screen</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    justifyContent: 'center',
    alignItems: 'center',
  },
  text: {
    color: '#fff',
  },
});

Внутри src/app/_layout.tsx:
Добавьте компонент и проп для обновления названия маршрута.<Stack.Screen />options/about
Обновите название маршрута, добавив проп./indexHomeoptions

import { Stack } from 'expo-router';

export default function RootLayout() {
  return (
    <Stack>
      <Stack.Screen name="index" options={{ title: 'Home' }} />
      <Stack.Screen name="about" options={{ title: 'About' }} />
    </Stack>
  );
}

### 2 Навигация между экранами
Мы используем компонент Expo Router для навигации от маршрута к маршруту. Это компонент React, который рендерит a с заданным проп.Link/index/about<Text>href

Импортируйте компонент изнутри src/app/index.tsx.Linkexpo-router
Добавляйте компонент за компонентом и пропускайте проп вместе с маршрутом.Link<Text>href/about
Добавьте стиль , и в компонент. Он требует тех же реквизитов, что и компонент.fontSizetextDecorationLinecolorLink<Text>
src/app/index.tsx

import { Text, View, StyleSheet } from 'react-native';
import { Link } from 'expo-router';

export default function Index() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Home screen</Text>
      <Link href="/about" style={styles.button}>
        Go to About screen
      </Link>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    color: '#fff',
  },
  button: {
    fontSize: 20,
    textDecorationLine: 'underline',
    color: '#fff',
  },
});

### 3 Добавьте маршрут, который не найден
Если маршрута нет, мы можем использовать маршрут для отображения экрана запасного варианта. Это полезно, когда мы хотим показывать пользовательский экран при навигации по неправильному маршруту на мобильном устройстве, вместо того чтобы вылетать приложение или отображать ошибку 404 в интернете. Expo Router использует специальный файл +not-found.tsx для обработки этого случая.+not-found

Создайте новый файл с именем +not-found.tsx внутри каталога src/app, чтобы добавить компонент.NotFoundScreen
Добавьте реквизит из кнопки для отображения пользовательского экрана для этого маршрута.optionsStack.Screen
Добавьте компонент для навигации по маршруту, который является нашим запасным маршрутом.Link/
src/app/+not-found.tsx

import { View, StyleSheet } from 'react-native';
import { Link, Stack } from 'expo-router';

export default function NotFoundScreen() {
  return (
    <>
      <Stack.Screen options={{ title: 'Oops! Not Found' }} />
      <View style={styles.container}>
        <Link href="/" style={styles.button}>
          Go back to Home screen!
        </Link>
      </View>
    </>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    justifyContent: 'center',
    alignItems: 'center',
  },

  button: {
    fontSize: 20,
    textDecorationLine: 'underline',
    color: '#fff',
  },
});

Чтобы проверить это, перейдите к URL в веб-браузере, так как там легко изменить путь URL. Приложение должно отображать компонент:http:localhost:8081/123NotFoundScreen

### 4 Добавьте навигатор нижней вкладки

Мы добавим навигатор по нижней вкладке в наше приложение и повторно используем существующие экраны «Домой» и «О нас» для создания макета вкладок. Мы также используем навигатор стека в корневом макете, чтобы маршрут отображался поверх любых других вложенных навигаторов.+not-found

1. Внутри каталога src/app добавьте подкаталог (вкладки). Эта специальная директория используется для группировки маршрутов и их отображения в нижней панели вкладок.
2. Создайте файл (tabs)/_layout.tsx внутри каталога. Он будет использоваться для определения раскладки вкладок, который отличается от корневого макета.
3. Переместите существующие файлы index.tsx и about.tsx внутри папки (вкладки). Структура каталога 

Обновите корневой файл макета, чтобы добавить маршрут:(tabs)

import { Stack } from 'expo-router';

export default function RootLayout() {
  return (
    <Stack>
      <Stack.Screen name="(tabs)" options={{ headerShown: false }} />
    </Stack>
  );
}
Внутри (tabs)/_layout.tsx добавьте компонент для определения расположения нижней вкладки:Tabs

import { Tabs } from 'expo-router';

export default function TabLayout() {
  return (
    <Tabs>
      <Tabs.Screen name="index" options={{ title: 'Home' }} />
      <Tabs.Screen name="about" options={{ title: 'About' }} />
    </Tabs>
  );
}

---

## Построение экрана

### 1 Разбор экрана

Прежде чем создавать этот экран с помощью кода, давайте разберём его на основные элементы.

Есть два основных элемента:
- В центре экрана отображается большое изображение
- В нижней части экрана расположены две кнопки

Первая кнопка содержит несколько компонентов. Родительский элемент имеет жёлтую рамку и содержит иконку и текстовые компоненты внутри строки.

### 2 Показ изображений

Мы будем использовать библиотеку для отображения изображения в приложении. Он предоставляет кроссплатформенный компонент для загрузки и рендеринга изображения. Он уже включен в стандартный шаблон проекта, который мы используем.expo-image<Image>

Компонент Image принимает источник изображения в качестве своего значения. Исходный код может быть как статическим активом, так и URL. Например, исходный код, требуемый из каталога ассетов/изображений, является статичным. Он также может поступать из сети как объект.uri

Чтобы использовать компонент Image в файле src/app/(tabs)/index.tsx:

1. Импортируйте из библиотеки.Imageexpo-image
2. Создайте переменную, чтобы использовать ассеты/изображения/background-image.png файл в качестве проппа компонента.PlaceholderImagesourceImage

import { View, StyleSheet } from 'react-native';
import { Image } from 'expo-image';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <Image source={PlaceholderImage} style={styles.image} />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});

### 3 Разделить компоненты на файлы

Давайте разделим код на несколько файлов по мере добавления новых компонентов на этот экран. В течение этого урока мы будем использовать каталог компонентов для создания пользовательских компонентов.

1. Создайте каталог компонентов внутри src, а внутри него — файл image-viewer.tsx.
2. Переместите код, чтобы отображать изображение в этом файле вместе со стилями.image

import { ImageSourcePropType, StyleSheet } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  imgSource: ImageSourcePropType;
};

export default function ImageViewer({ imgSource }: Props) {
  return <Image source={imgSource} style={styles.image} />;
}

const styles = StyleSheet.create({
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});

Импортируйте и используйте его в src/app/(tabs)/index.tsx:ImageViewer

import { StyleSheet, View } from 'react-native';

import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
});

### 4 Создайте кнопки с помощью Pressable

React Native включает несколько различных компонентов для обработки сенсорных событий, но <Pressable> рекомендуется за свою гибкость. Он может обнаруживать одиночные нажатия, долгие нажатия, запускать отдельные события при нажатии и отпускании кнопки и многое другое.

В дизайне нам нужно создать две кнопки. У каждого свой стиль и ярлык. Давайте начнём с создания многоразового компонента для этих кнопок. Создайте файл button.tsx внутри каталога src/components с помощью следующего кода:

import { StyleSheet, View, Pressable, Text } from 'react-native';

type Props = {
  label: string;
};

export default function Button({ label }: Props) {
  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});

Приложение показывает оповещение при нажатии любой из кнопок на экране. Это происходит из-за призывов к его реквизиту. Давайте импортируем этот компонент в файл src/app/(tabs)/index.tsx и добавим стили, которые инкапсулируют эти кнопки:<Pressable>alert()onPress<View>

import { View, StyleSheet } from 'react-native';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require("@/assets/images/background-image.png");

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button label="Choose a photo" />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});

### 5 Улучшите компонент многоразовой кнопки

Кнопка «Выбрать фото» требует другого стиля, чем кнопка «Использовать эту фотографию», поэтому мы добавим новый реквизит для темы кнопок, который позволит применить тему. Эта кнопка также имеет иконку перед этикеткой. Мы используем иконку из библиотеки.primary@expo/vector-icons

Чтобы загрузить и отобразить значок на кнопке, давайте воспользуемся из библиотеки. Измените src/components/button.tsx, чтобы добавить следующий фрагмент кода:FontAwesome

import { StyleSheet, View, Pressable, Text } from 'react-native';
import FontAwesome from '@expo/vector-icons/FontAwesome';

type Props = {
  label: string;
  theme?: 'primary';
};

export default function Button({ label, theme }: Props) {
  if (theme === 'primary') {
  return (
      <View
        style={[
          styles.buttonContainer,
          { borderWidth: 4, borderColor: '#ffd33d', borderRadius: 18 },
        ]}>
        <Pressable
          style={[styles.button, { backgroundColor: '#fff' }]}
          onPress={() => alert('You pressed a button.')}>
          <FontAwesome name="picture-o" size={18} color="#25292e" style={styles.buttonIcon} />
          <Text style={[styles.buttonLabel, { color: '#25292e' }]}>{label}</Text>
        </Pressable>
      </View>
    );
  }

  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonIcon: {
    paddingRight: 8,
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});

Давайте узнаем, что делает вышеуказанный код:

Кнопка основной темы использует встроенные стили, которые переопределяют стили, определённые в предмете, непосредственно передающем в реквизит.StyleSheet.create()style
Компонент в основной теме использует свойство с значением, чтобы задать фон кнопки белым. Если добавить это свойство к , значение цвета фона будет установлено как для основной, так и для нестилизованной.<Pressable>backgroundColor#fffstyles.button
Встроенные стили используют JavaScript и переопределяют стандартные стили для определённого значения.
Теперь измените файл src/app/(tabs)/index.tsx, чтобы использовать проп на первой кнопке.theme="primary"

import { View, StyleSheet } from 'react-native';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});

---

## Использования набора изображений

React Native предоставляет встроенные компоненты в качестве стандартных строительных блоков, такие как , , и . Мы создаём функцию для выбора изображения из медиагалереи устройства. Это невозможно с основными компонентами, и нам понадобится библиотека, чтобы добавить эту функцию в наше приложение.<View><Text><Pressable>

Мы используем expo-image-picker, библиотеку от Expo SDK.

### 1 Установка expo-image-picker

Чтобы установить библиотеку, остановите сервер разработки, нажав + в терминале, затем выполните следующую команду:expo-image-pickerCtrlC

npx expo install expo-image-picker
The npx expo install Команда установит библиотеку и добавит её в зависимости проекта в package.json.

### 2 Выбор изображения из медиабиблиотеки устройства
expo-image-picker предоставляет способ отображения системного интерфейса путём выбора изображения или видео из медиатеки устройства. Мы используем основную тематическую кнопку, созданную в предыдущей главе, чтобы выбрать изображение из медиабиблиотеки устройства и создать функцию запуска библиотеки изображений устройства для реализации этой функции.launchImageLibraryAsync()

В src/app/(tabs)/index.tsx импортируйте библиотеку и создайте функцию внутри компонента:expo-image-pickerpickImageAsync()Index

import * as ImagePicker from 'expo-image-picker';

export default function Index() {
  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      console.log(result);
    } else {
      alert('You did not select any image.');
    }
  };

}
Давайте узнаем, что делает вышеуказанный код:
Он получает объект для указания различных опций. Этот объект — это launchImageLibraryAsync()ImagePickerOptions Объект, который мы проходим при вызове метода.
При установке на , пользователь может обрезать изображение во время выбора на Android и iOS.allowsEditingtrue

### 3 Обновить компонент кнопок
При нажатии основной кнопки мы вызовем функцию компонента. Обновите проп компонента в src/components/button.tsx:pickImageAsync()ButtononPressButton

import { StyleSheet, View, Pressable, Text } from 'react-native';
import FontAwesome from '@expo/vector-icons/FontAwesome';

type Props = {
  label: string;
  theme?: 'primary';
  onPress?: () => void;
};

export default function Button({ label, theme, onPress }: Props) {
  if (theme === 'primary') {
    return (
      <View
        style={[
          styles.buttonContainer,
          { borderWidth: 4, borderColor: '#ffd33d', borderRadius: 18 },
        ]}>
        <Pressable style={[styles.button, { backgroundColor: '#fff' }]} onPress={onPress}>
          <FontAwesome name="picture-o" size={18} color="#25292e" style={styles.buttonIcon} />
          <Text style={[styles.buttonLabel, { color: '#25292e' }]}>{label}</Text>
        </Pressable>
      </View>
    );
  }

  return (
    <View style={styles.buttonContainer}>
      <Pressable style={styles.button} onPress={() => alert('You pressed a button.')}>
        <Text style={styles.buttonLabel}>{label}</Text>
      </Pressable>
    </View>
  );
}

const styles = StyleSheet.create({
  buttonContainer: {
    width: 320,
    height: 68,
    marginHorizontal: 20,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 3,
  },
  button: {
    borderRadius: 10,
    width: '100%',
    height: '100%',
    alignItems: 'center',
    justifyContent: 'center',
    flexDirection: 'row',
  },
  buttonIcon: {
    paddingRight: 8,
  },
  buttonLabel: {
    color: '#fff',
    fontSize: 16,
  },
});

В src/app/(tabs)/index.tsx добавьте функцию в проп на первом .pickImageAsync()onPress<Button>

import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      console.log(result);
    } else {
      alert('You did not select any image.');
    }
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});

Функция вызывает и затем обрабатывает результат. Метод возвращает объект с информацией о выбранном изображении.pickImageAsync()ImagePicker.launchImageLibraryAsync()launchImageLibraryAsync()

Вот пример объекта и свойств, которые он содержит:result
{
  "assets": [
    {
      "assetId": null,
      "base64": null,
      "duration": null,
      "exif": null,
      "fileName": "ea574eaa-f332-44a7-85b7-99704c22b402.jpeg",
      "fileSize": 4513577,
      "height": 4570,
      "mimeType": "image/jpeg",
      "rotation": null,
      "type": "image",
      "uri": "file:///data/user/0/host.exp.exponent/cache/ExperienceData/%2540anonymous%252FStickerSmash-13f21121-fc9d-4ec6-bf89-bf7d6165eb69/ImagePicker/ea574eaa-f332-44a7-85b7-99704c22b402.jpeg",
      "width": 2854

### 4 Используйте выбранное изображение
Объект предоставляет массив выбранного изображения. Давайте возьмём это значение из picker изображений и используем его, чтобы показать выбранное изображение в приложении.resultassetsuri

Измените файл src/app/(tabs)/index.tsx:

1. Объявим переменную состояния, вызванную с помощью selectedImageuseState крючок от React. Мы используем эту переменную состояния, чтобы сохранить URI выбранного изображения.
2. Обновите функцию, чтобы сохранить URI изображения в переменной состояния.pickImageAsync()selectedImage
3. Передайте его как реквизит компоненту.selectedImageImageViewer

import { View, StyleSheet } from 'react-native';
import * as ImagePicker from 'expo-image-picker';
import { useState } from 'react';

import Button from '@/components/button';
import ImageViewer from '@/components/image-viewer';

const PlaceholderImage = require('@/assets/images/background-image.png');

export default function Index() {
  const [selectedImage, setSelectedImage] = useState<string | undefined>(undefined);

  const pickImageAsync = async () => {
    let result = await ImagePicker.launchImageLibraryAsync({
      mediaTypes: ['images'],
      allowsEditing: true,
      quality: 1,
    });

    if (!result.canceled) {
      setSelectedImage(result.assets[0].uri);
    } else {
      alert('You did not select any image.');
    }
  };

  return (
    <View style={styles.container}>
      <View style={styles.imageContainer}>
        <ImageViewer imgSource={PlaceholderImage} selectedImage={selectedImage} />
      </View>
      <View style={styles.footerContainer}>
        <Button theme="primary" label="Choose a photo" onPress={pickImageAsync} />
        <Button label="Use this photo" />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#25292e',
    alignItems: 'center',
  },
  imageContainer: {
    flex: 1,
  },
  footerContainer: {
    flex: 1 / 3,
    alignItems: 'center',
  },
});

Передайте реквизит компоненту, чтобы отобразить выбранное изображение вместо временного изображения.selectedImageImageViewer

1. Модифицируйте файл src/components/image-viewer.tsx, чтобы он принял проп.selectedImage
2. Источник изображения становится длинным, поэтому давайте также переместим его в отдельную переменную под названием .imageSource
3. Передайте как значение пропеллера на компоненте.imageSourcesourceImage

import { ImageSourcePropType, StyleSheet } from 'react-native';
import { Image } from 'expo-image';

type Props = {
  imgSource: ImageSourcePropType;
  selectedImage?: string;
};

export default function ImageViewer({ imgSource, selectedImage }: Props) {
  const imageSource = selectedImage ? { uri: selectedImage } : imgSource;

  return <Image source={imageSource} style={styles.image} />;
}

const styles = StyleSheet.create({
  image: {
    width: 320,
    height: 440,
    borderRadius: 18,
  },
});

В приведённом выше фрагменте компонент Image использует условный оператор для загрузки исходного источника изображения. Выбранное изображение — это uri Строка, а не локальный актив, как заполняющее изображение.

---