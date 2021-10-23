# -*- encoding: utf-8 -*-
import random
import unreal


class UnrealCore(object):
    """the unreal base class"""

    def __init__(self):
        self.unreal = unreal

    def create_folder(self, folder_path):
        """创建文件夹
        Args:
            folder_path (str): the path of a folder
        """
        return self.unreal.EditorAssetLibrary.make_directory(folder_path)

    def set_folder_color(self, folder_path, color):
        """设置文件夹的颜色
        Args:
            folder_path (str): the path of a folder
            color (tuple): the tuple of color value
        """
        return self.unreal.CppLib.set_folder_color(folder_path, color)


def create_set_folder_color(folder_dir):
    """创建和设置文件夹的颜色
    Args:
        folder_dir (str): the dir of a folder
    """
    unreal_core = UnrealCore()
    for num in range(100, 150):
        random_color = (random.random(), random.random(), random.random(), 1)
        folder_path = "{}/Asset_{}".format(folder_dir, str(num))
        # unreal_core.set_folder_color(folder_path, random_color)
        unreal_core.create_folder(folder_path)


if __name__ == '__main__':
    folder_dir = "/Game/Assets/"
    create_set_folder_color(folder_dir)
