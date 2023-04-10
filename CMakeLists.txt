cmake_minimum_required(VERSION 3.16)
project(RADB VERSION 0.1 LANGUAGES C CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt5 Qt6 REQUIRED COMPONENTS Core)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Widgets Gui Network)

qt_standard_project_setup()

qt_add_executable(RADB WIN32 MACOSX_BUNDLE
    classes/animation.cpp classes/animation.h
    classes/application.cpp classes/application.h
    classes/computer.cpp classes/computer.h
    classes/ecwin7.cpp classes/ecwin7.h
    classes/models/apptablemodel.cpp classes/models/apptablemodel.h
    classes/models/backuptablemodel.cpp classes/models/backuptablemodel.h
    classes/models/contactmodel.cpp classes/models/contactmodel.h
    classes/models/filetablemodel.cpp classes/models/filetablemodel.h
    classes/models/logcatmodel.cpp classes/models/logcatmodel.h
    classes/models/messagemodel.cpp classes/models/messagemodel.h
    classes/models/messagethreadmodel.cpp classes/models/messagethreadmodel.h
    classes/mytableview.cpp classes/mytableview.h
    classes/phone.cpp classes/phone.h
    classes/updateapp.cpp classes/updateapp.h
#    dialogs/aboutdialog.cpp dialogs/aboutdialog.h dialogs/aboutdialog.ui
#    dialogs/appdialog.cpp dialogs/appdialog.h dialogs/appdialog.ui
#    dialogs/appinfo.cpp dialogs/appinfo.h dialogs/appinfo.ui
#    dialogs/connectWifi.cpp dialogs/connectWifi.h dialogs/connectWifi.ui
#    dialogs/dialogkopiuj.cpp dialogs/dialogkopiuj.h dialogs/dialogkopiuj.ui
#    dialogs/logcatdialog.cpp dialogs/logcatdialog.h dialogs/logcatdialog.ui
    dialogs/mainwindow.cpp dialogs/mainwindow.h dialogs/mainwindow.ui
#    dialogs/registerdialog.cpp dialogs/registerdialog.h dialogs/registerdialog.ui
    main.cpp
#    threads/screenshotthread.cpp threads/screenshotthread.h
#    widgets/appwidget.cpp widgets/appwidget.h widgets/appwidget.ui
#    widgets/contactwidget.cpp widgets/contactwidget.h widgets/contactwidget.ui
#    widgets/fastbootwidget.cpp widgets/fastbootwidget.h widgets/fastbootwidget.ui
#    widgets/filewidget.cpp widgets/filewidget.h widgets/filewidget.ui
#    widgets/messagewidget.cpp widgets/messagewidget.h widgets/messagewidget.ui
#    widgets/phoneinfowidget.cpp widgets/phoneinfowidget.h widgets/phoneinfowidget.ui
#    widgets/recoverywidget.cpp widgets/recoverywidget.h widgets/recoverywidget.ui
#    widgets/screenshotwidget.cpp widgets/screenshotwidget.h widgets/screenshotwidget.ui
#    widgets/settingswidget.cpp widgets/settingswidget.h widgets/settingswidget.ui
#    widgets/shellwidget.cpp widgets/shellwidget.h widgets/shellwidget.ui
)
target_link_libraries(RADB PRIVATE
    Qt::Core
    Qt::Widgets
    Qt::Gui
    Qt::Network
    declarative
)


# Resources:
set_source_files_properties("images/android.ico"
    PROPERTIES QT_RESOURCE_ALIAS "android.ico"
)
set_source_files_properties("images/android.png"
    PROPERTIES QT_RESOURCE_ALIAS "android.png"
)
set_source_files_properties("images/appBrain.png"
    PROPERTIES QT_RESOURCE_ALIAS "appBrain.png"
)
set_source_files_properties("images/apps.png"
    PROPERTIES QT_RESOURCE_ALIAS "apps.png"
)
set_source_files_properties("images/backup.png"
    PROPERTIES QT_RESOURCE_ALIAS "backup.png"
)
set_source_files_properties("images/computer.png"
    PROPERTIES QT_RESOURCE_ALIAS "computer.png"
)
set_source_files_properties("images/contactDefault.png"
    PROPERTIES QT_RESOURCE_ALIAS "contactDefault.png"
)
set_source_files_properties("images/contacts.png"
    PROPERTIES QT_RESOURCE_ALIAS "contacts.png"
)
set_source_files_properties("images/copy.png"
    PROPERTIES QT_RESOURCE_ALIAS "copy.png"
)
set_source_files_properties("images/fastboot.png"
    PROPERTIES QT_RESOURCE_ALIAS "fastboot.png"
)
set_source_files_properties("images/files.png"
    PROPERTIES QT_RESOURCE_ALIAS "files.png"
)
set_source_files_properties("images/find.png"
    PROPERTIES QT_RESOURCE_ALIAS "find.png"
)
set_source_files_properties("images/hidden.png"
    PROPERTIES QT_RESOURCE_ALIAS "hidden.png"
)
set_source_files_properties("images/info.png"
    PROPERTIES QT_RESOURCE_ALIAS "info.png"
)
set_source_files_properties("images/install.png"
    PROPERTIES QT_RESOURCE_ALIAS "install.png"
)
set_source_files_properties("images/logcat.png"
    PROPERTIES QT_RESOURCE_ALIAS "logcat.png"
)
set_source_files_properties("images/market.png"
    PROPERTIES QT_RESOURCE_ALIAS "market.png"
)
set_source_files_properties("images/messages.png"
    PROPERTIES QT_RESOURCE_ALIAS "messages.png"
)
set_source_files_properties("images/newDir.png"
    PROPERTIES QT_RESOURCE_ALIAS "newDir.png"
)
set_source_files_properties("images/paypal.png"
    PROPERTIES QT_RESOURCE_ALIAS "paypal.png"
)
set_source_files_properties("images/phone.png"
    PROPERTIES QT_RESOURCE_ALIAS "phone.png"
)
set_source_files_properties("images/recovery.png"
    PROPERTIES QT_RESOURCE_ALIAS "recovery.png"
)
set_source_files_properties("images/refresh.png"
    PROPERTIES QT_RESOURCE_ALIAS "refresh.png"
)
set_source_files_properties("images/remove.png"
    PROPERTIES QT_RESOURCE_ALIAS "remove.png"
)
set_source_files_properties("images/rename.png"
    PROPERTIES QT_RESOURCE_ALIAS "rename.png"
)
set_source_files_properties("images/restore.png"
    PROPERTIES QT_RESOURCE_ALIAS "restore.png"
)
set_source_files_properties("images/rotate-left.png"
    PROPERTIES QT_RESOURCE_ALIAS "rotate-left.png"
)
set_source_files_properties("images/rotate-right.png"
    PROPERTIES QT_RESOURCE_ALIAS "rotate-right.png"
)
set_source_files_properties("images/save.png"
    PROPERTIES QT_RESOURCE_ALIAS "save.png"
)
set_source_files_properties("images/screenshot.png"
    PROPERTIES QT_RESOURCE_ALIAS "screenshot.png"
)
set_source_files_properties("images/selectAll.png"
    PROPERTIES QT_RESOURCE_ALIAS "selectAll.png"
)
set_source_files_properties("images/selectNone.png"
    PROPERTIES QT_RESOURCE_ALIAS "selectNone.png"
)
set_source_files_properties("images/settings.png"
    PROPERTIES QT_RESOURCE_ALIAS "settings.png"
)
set_source_files_properties("images/shell.png"
    PROPERTIES QT_RESOURCE_ALIAS "shell.png"
)
set_source_files_properties("images/uninstall.png"
    PROPERTIES QT_RESOURCE_ALIAS "uninstall.png"
)
set(zasoby_resource_files
    "images/android.ico"
    "images/android.png"
    "images/appBrain.png"
    "images/apps.png"
    "images/backup.png"
    "images/computer.png"
    "images/contactDefault.png"
    "images/contacts.png"
    "images/copy.png"
    "images/fastboot.png"
    "images/files.png"
    "images/find.png"
    "images/help.png"
    "images/hidden.png"
    "images/info.png"
    "images/install.png"
    "images/logcat.png"
    "images/market.png"
    "images/messages.png"
    "images/newDir.png"
    "images/paypal.png"
    "images/phone.png"
    "images/recovery.png"
    "images/refresh.png"
    "images/remove.png"
    "images/rename.png"
    "images/restore.png"
    "images/rotate-left.png"
    "images/rotate-right.png"
    "images/save.png"
    "images/screenshot.png"
    "images/selectAll.png"
    "images/selectNone.png"
    "images/settings.png"
    "images/shell.png"
    "images/uninstall.png"
)

qt_add_resources(RADB "zasoby"
    PREFIX
        "/icons"
    FILES
        ${zasoby_resource_files}
)
set_source_files_properties("languages/radb_ar.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_ar.qm"
)
set_source_files_properties("languages/radb_cs.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_cs.qm"
)
set_source_files_properties("languages/radb_de.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_de.qm"
)
set_source_files_properties("languages/radb_el.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_el.qm"
)
set_source_files_properties("languages/radb_en.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_en.qm"
)
set_source_files_properties("languages/radb_es.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_es.qm"
)
set_source_files_properties("languages/radb_hu.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_hu.qm"
)
set_source_files_properties("languages/radb_it.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_it.qm"
)
set_source_files_properties("languages/radb_ja.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_ja.qm"
)
set_source_files_properties("languages/radb_nl.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_nl.qm"
)
set_source_files_properties("languages/radb_pl.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_pl.qm"
)
set_source_files_properties("languages/radb_pt.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_pt.qm"
)
set_source_files_properties("languages/radb_ru.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_ru.qm"
)
set_source_files_properties("languages/radb_sr.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_sr.qm"
)
set_source_files_properties("languages/radb_sv.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_sv.qm"
)
set_source_files_properties("languages/radb_zh.qm"
    PROPERTIES QT_RESOURCE_ALIAS "radb_zh.qm"
)
set(zasoby1_resource_files
    "languages/radb_ar.qm"
    "languages/radb_cs.qm"
    "languages/radb_de.qm"
    "languages/radb_el.qm"
    "languages/radb_en.qm"
    "languages/radb_es.qm"
    "languages/radb_hu.qm"
    "languages/radb_it.qm"
    "languages/radb_ja.qm"
    "languages/radb_nl.qm"
    "languages/radb_pl.qm"
    "languages/radb_pt.qm"
    "languages/radb_ru.qm"
    "languages/radb_sr.qm"
    "languages/radb_sv.qm"
    "languages/radb_zh.qm"
)

qt_add_resources(RADB "zasoby1"
    PREFIX
        "/lang"
    FILES
        ${zasoby1_resource_files}
)
set(zasoby2_resource_files
#    "qml/messageView.qml"
#    "qml/messages/ContactList.qml"
#    "qml/messages/MessageList.qml"
#    "qml/messages/NewMessage.qml"
#    "qml/messages/ThreadList.qml"
#    "qml/messages/delegates/Button.qml"
#    "qml/messages/delegates/ContactDelegate.qml"
#    "qml/messages/delegates/MessageDelegate.qml"
#    "qml/messages/delegates/ScrollBar.qml"
#    "qml/messages/delegates/SendMessage.qml"
#    "qml/messages/delegates/SendSmsButton.qml"
#    "qml/messages/delegates/ThreadContextMenu.qml"
#    "qml/messages/delegates/ThreadDelegate.qml"
)

qt_add_resources(RADB "zasoby2"
    PREFIX
        "/qml"
    FILES
        ${zasoby2_resource_files}
)

if(WIN32)
    target_link_libraries(RADB PRIVATE
        libole32
    )
endif()

install(TARGETS RADB
    BUNDLE DESTINATION .
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)

qt_generate_deploy_app_script(
    TARGET RADB
    FILENAME_VARIABLE deploy_script
    NO_UNSUPPORTED_PLATFORM_ERROR
)
install(SCRIPT ${deploy_script})
