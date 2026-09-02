<img width="434" height="349" alt="player_jump" src="https://github.com/user-attachments/assets/05d78dd8-4dce-45dc-bf88-3da338e6dac3" />
<img width="343" height="370" alt="player_attack" src="https://github.com/user-attachments/assets/156055d6-aea8-4452-a135-2f3b53b1e2e7" />
<img width="217" height="409" alt="player_idle" src="https://github.com/user-attachments/assets/7990aeca-96a8-40c1-8cb3-e52859c68443" />


import os

try:
    # Get the directory where this script is located
    script_directory = os.path.dirname(__file__)
    print(f"--- Diagnostic Information ---")
    print(f"✅ Script is running in this folder:\n   {script_directory}\n")

    # This is the full path where the script is looking for the 'assets' folder
    assets_path = os.path.join(script_directory, 'assets')
    print(f"👀 Script is looking for the assets folder at this exact path:\n   {assets_path}\n")

    # Check what files/folders are in the main directory
    print(f"📁 Contents of the script's folder:")
    for item in os.listdir(script_directory):
        print(f"   - {item}")
    print("")

    # Check if the 'assets' folder exists
    if os.path.isdir(assets_path):
        print(f"✔️ SUCCESS: Found the 'assets' folder!")
        print(f"🖼️ Contents of the 'assets' folder:")
        asset_contents = os.listdir(assets_path)
        if not asset_contents:
            print("   - The 'assets' folder is empty.")
        else:
            for item in asset_contents:
                print(f"   - {item}")
    else:
        print(f"❌ ERROR: The 'assets' folder was NOT found at the expected path.")
        print(f"   Please make sure a folder named 'assets' (all lowercase) exists in the same directory as your scripts.")

except Exception as e:
    print(f"An unexpected error occurred: {e}")

print("\n--- End of Report ---")

